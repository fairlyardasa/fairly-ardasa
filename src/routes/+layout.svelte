<script>
// @ts-nocheck

    import { onMount } from "svelte";
    import { gsap } from 'gsap/dist/gsap';
    import "../app.css";
    import { Power2 } from "gsap";
    import Lenis from 'lenis';
    import {ScrollTrigger} from 'gsap/dist/ScrollTrigger'
    import {CSSRulePlugin} from 'gsap/dist/CSSRulePlugin'
    import { annotate, annotationGroup } from 'rough-notation';

    

    onMount(() => {
        const smallerScreen = window.innerWidth < 768;

        gsap.registerPlugin(ScrollTrigger, CSSRulePlugin);

        const tl = gsap.timeline({ paused: true });
        let path = document.querySelector(".overlay path");
        let spanBefore = CSSRulePlugin.getRule("#hamburger span:before");

        gsap.set(spanBefore, { background: "rgb(59,130,246)" });
        gsap.set(".menu", { visibility: "hidden" });
       


       

        

        function revealMenu() {
            revealMenuItems();

            const hamburger = document.getElementById("hamburger");
            const toogleBtn = document.getElementById("toogle-btn");
            const navBtn1 = document.getElementsByClassName("nav")[0];
            const navBtn2 = document.getElementsByClassName("nav")[1];
            const navBtn3 = document.getElementsByClassName("nav")[2];

            

            
            if (toogleBtn && hamburger) {
            toogleBtn.onclick = function (e) {
            hamburger.classList.toggle("active");
            tl.reversed(!tl.reversed());}
            }

            if (hamburger) {
            navBtn1.onclick = function () {
            hamburger.classList.toggle("active"); 
            tl.reversed(!tl.reversed());
            };
            navBtn2.onclick = function () {
            hamburger.classList.toggle("active"); 
            tl.reversed(!tl.reversed());
            };
            navBtn3.onclick = function () {
            hamburger.classList.toggle("active"); 
            tl.reversed(!tl.reversed());
            };
            } 
        }

        revealMenu();

        function revealMenuItems(){
            const start = "M0 502S175 272 500 272s500 230 500 230V0H0Z";
            const end = "M0 2S175 1 500 1s500 1 500 1V0H0Z ";

            const power2 ="power2.inOut";
            const power4 ="power4.inOut";

            
            tl.to('#hamburger span',1, {
                background: "#313131",
                ease: power2
            },"<"
            ); 

            tl.to(spanBefore,1, {
                background: "#313131",
                ease: power2
            },"<"
            ); 

            if (smallerScreen) {

                tl.to('.btn .btn-outline',1.25, {
                width: "80px",
                height: "80px",
                border: "1px solid #313131",
                ease: power4
                },"<");

                tl.to('#hamburger',1.25, {
                    marginTop: "-5px",
                    ease: power4
                });
                
            } else {

                tl.to('.btn .btn-outline',1.25, {
                x: -40,
                y: 40,
                width: "140px",
                height: "140px",
                border: "1px solid #313131",
                ease: power4
                },"<");

                tl.to('#hamburger',1.25, {
                    marginTop: "-5px",
                    x: -40,
                    y: 40,
                    ease: power4
                });
                
            }
            

            

            tl.to(path, 0.8, {
               attr: {
                d: start,
               },
               ease: power2,
            },"<").to( path ,0.8, {
                attr:{
                    d: end
                },
                ease: Power2.easeOut
            }, "-0.5");

            tl.to(
                ".menu",
                1,
                {
                    visibility: "visible",
                    ease: power2

                },
                "-=0.5"
            )

            tl.to(
                ".menu-item > a", 
                1,
                {
                    top: 0,
                    ease: "power3.out",
                    stagger: {
                        amount: 0.5
                    }
                },
                "-=1"
            ).reverse();


        }

        
        
        const lenis = new Lenis();

        lenis.on("scroll", ScrollTrigger.update);

        gsap.ticker.add((time) =>{
            lenis.raf(time*1000)
        });

        gsap.ticker.lagSmoothing(0);

        const services = gsap.utils.toArray(".service");

        const observerOptions = {
            root: null,
            rootMargin: "0px",
            threshold: 0.1,

        };

        const observerCallback = (entries, observer) => {
            entries.forEach((entry)=> {
            if (entry.isIntersecting){
                const service = entry.target;
                const imgContainer = service.querySelector(".service-img img");

                ScrollTrigger.create({
                trigger: service,
                start: "bottom bottom",
                end: "top top",
                scrub: true,
                onUpdate: (self) => {
                    let progress = self.progress;
                    let newWidth = 60 + 40 * progress;

                    gsap.to(imgContainer, {
                    width: newWidth + "%",
                    duration: 0.1,
                    ease: "none"
                    })
                }
                
                });

                ScrollTrigger.create({
                trigger: service,
                start: "top bottom",
                end:"top top",
                scrub: true,
                onUpdate: (self) => {
                    let progress = self.progress;
                    let newHeight = 40 + 60 * progress;
                    gsap.to(service,{
                    height: newHeight + "%",
                    duration: 0.1,
                    ease: "none"
                    })
                }
                });

                observer.unobserve(service);
            }
            })
        };

        const observer = new IntersectionObserver(observerCallback, observerOptions);

        services.forEach((service)=>{
            observer.observe(service);
        })


    });

</script>
<slot />


<div class="btn m-5" id="toogle-btn">
    <div class="btn-outline btn-outline-1">
    </div>
    <div class="btn-outline btn-outline-2">
    </div>
    <div id="hamburger">
    <span></span>
    </div>
</div>



<div class="overlay">
    <svg viewBox="0 0 1000 1000">
        <path d="M0 0S175 0 500 0s500 0 500 0V0H0Z "></path>
    </svg>
</div>

<div class="menu">
    <div class="primary-menu">
        <div class="menu-container">
            <div class="wrapper">
                <div class="menu-item">
                    <a class="nav" href="#hero"><span>I</span>Home</a>
                    <div class="menu-iten-revealer"></div>
                </div>

                <div class="menu-item">
                    <a class="nav" href="#aboutme"><span>II</span>About</a>
                    <div class="menu-iten-revealer"></div>
                </div>

                <div class="menu-item">
                    <a class="nav" href="#projects"><span>III</span>Projects</a>
                    <div class="menu-iten-revealer"></div>
                </div>


            </div>
        </div>
    </div>

    <div class="secondary-menu">
        <div class="menu-container">
            <div class="wrapper">
            </div>
        </div>
    </div>

    

</div>
