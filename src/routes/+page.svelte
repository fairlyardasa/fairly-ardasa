<script>
// @ts-nocheck

import image from '../lib/images/Maskgroup.png';
import cssLogo from '../lib/images/css-logo.png';
import jsLogo from '../lib/images/js-logo.png';
import htmlLogo from '../lib/images/html-logo.png';
import svelteLogo from '../lib/images/svelte-logo.png';
import tsLogo from '../lib/images/ts-logo.png';
import vueLogo from '../lib/images/vue-logo.png';
import laravelLogo from '../lib/images/laravel-logo.png';
import qrCode from '../lib/images/qr-code.png';

import kurJogja from '../lib/images/my-project/kur-jogja.png'
import Lokadwaya from '../lib/images/my-project/lokadwaya.png'
import Spotless from '../lib/images/my-project/spotless.png'
import  AOS  from "aos";
import { onMount } from 'svelte';

onMount(() => {
		AOS.init()
	})

</script>

<svelte:head>
	<link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />
</svelte:head>

<section class="hero text-gray-600 body-font" id="hero">
    <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
      <div class="lg:max-w-lg lg:w-full md:w-1/3 w-3/6 mb-10 md:mb-0">
        <img data-aos="fade-right" data-aos-duration="3000" class="object-cover object-center rounded-full border-2 border-black m-4" width="80%" alt="hero" src={image}>
      </div>
      <div data-aos="fade-down" data-aos-duration="2000" id="myname" class="lg:flex-grow md:w-1/2 lg:pl-24 md:pl-16 flex flex-col md:items-start md:text-left items-center text-center">
        <h1   class="title-font sm:text-7xl text-3xl font-black text-white-primary mb-3">I’m Fairly Ardasa</h1>
        <h2 class="title-font sm:text-2xl text-xl mb-10 font-medium text-blue-500 italic">Front End Developer</h2>
        <p class="leading-relaxed w-11/12 text-white-primary">Hardworking and enthusiastic <span id="college-student">College Student</span> working towards a <span>Front End Developer</span>. Able to effectively self-manage during independent projects, as well as collaborate in team setting.</p>
      </div>
    </div>
</section>


<section class=" text-gray-600 body-font" id="aboutme">
    <div class="container m-auto flex md:flex-col items-center">
      <div  class=" flex flex-col min-w-full px-2">
        <h1 class="aboutme sm:text-6xl text-3xl font-black text-white-primary text-center mt-10">about me</h1>
        <div class="border-t border-gray-300 my-6"></div>
        <div data-aos="fade-down" class="bg-white relative flex flex-wrap py-6 px-2 rounded shadow-md mx-2 ">
            <div class="lg:w-1/2 px-6 flex flex-col justify-between">
                <h1 class="sm:text-4xl text-3xl font-black ">Education.</h1>
              <p class="mt-4">I am a university student in the second year of my bachelor. Currently i’m looking for some internship to gain some experience for the working world later</p>
            </div>
            <ul class="lg:w-1/2 px-6 py-auto mt-4 lg:mt-0 justify-between list-disc">
                <li class="m-3">University Representative for Gemastik  XVI for Game Development Division</li>
                <li class="m-3">Member of UXGAMA</li>
                <li class="m-3">Software Engineering,Universitas Gadjah Mada</li>
            </ul>
        </div>
        <div data-aos="fade-down" class="bg-white relative flex flex-wrap mt-7  py-6 px-2 rounded shadow-md mx-2 ">
            <div class="lg:w-1/2 px-6 flex flex-col flex-wrap space-between">
                <h1 class="sm:text-4xl text-3xl font-black ">Skills.</h1>
                <p class="mt-4">As a software engineering student, I have been taught several skills in the IT field. Apart from being obtained from college, as for the skills I got from the projects I have worked on.</p>
                <ul class="px-6 py-auto mt-4 lg:mt-0 list-disc">
                  <li class="m-3">Web Development</li>
                  <li class="m-3">Mobile Apps Development</li>
                  <li class="m-3">UI/UX</li>
              </ul>
            </div>
            <div class="skills-icon lg:w-1/2 px-6 mt-4 lg:mt-0 flex flex-wrap gap-2 justify-around">
                <img src={htmlLogo} alt="HTML Logo" class="w-16 h-16">
                <img src={cssLogo} alt="CSS Logo" class="w-16 h-16">
                <img src={jsLogo} alt="JS Logo" class="w-16 h-16">
                <img src={svelteLogo} alt="Svelte Logo" class="w-16 h-16">
                <img src={tsLogo} alt="TS Logo" class="w-16 h-16">
                <img src={vueLogo} alt="Vue Logo" class="w-16 h-16">
                <img src={laravelLogo} alt="Laravel Logo" class="w-16 h-16">
            </div>
        </div>

        <div data-aos="fade-down" class="flex flex-row flex-wrap min-w-full lg:mt-20  justify-center ">
            <div class="lg:w-1/2 lg:mt-0 mt-10 w-full px-6 flex flex-col">
                <h1 class="sm:text-4xl text-3xl font-black text-white-primary ">curriculum vitae.</h1>
                <a href="https://drive.google.com/file/d/1X6w4-947SUbZGD9fPLrAxuiufYXDczSV/view?usp=drive_link"><img class="w-40 h-40 m-6" src={qrCode} alt="" srcset=""></a>
                
            </div>
            <div data-aos="fade-down" class="lg:w-1/2 lg:mt-0 mt-10 w-full px-6 flex flex-col text-white-primary">
                <h1 class="sm:text-4xl text-3xl font-black text-white-primary">languages.</h1>
                <div class="m-6">
                <div><span class="font-bold">native: </span> <span class="font-light"></span>indonesian</div>
                <div><span class="font-bold">others: </span> <span class="font-light"></span>english</div>
                </div>
            </div>
        </div>
    </div>
</section>

<section class="mt-12" id="projects">
  <div class="container max-w-max m-auto">
    <section class="hero-2">
      <section class="services">
        <div class="services-header">
          <div class="col justify-center"></div>
          <h1 class=" sm:text-6xl text-3xl font-black text-white-primary text-center my-10">my projects</h1>
        </div>

        <div class="service">
          <div class="service-info flex-grow">
            <div class="flex h-full flex-col flex-grow justify-between">
              <h1 class="sm:text-4xl text-3xl font-black ">kur jogja</h1>

              <p  class="text-white-primary font-light text-sm">
                Work closely with UI/UX designers to translate design wireframes into functional and aesthetically pleasing web components, ensuring the correct implementation of UI components, layouts, and visuals
              </p>
            </div>
          </div>
          <div class="service-img">
            <img src={kurJogja} alt="">
          </div>
        </div>

        <div class="service">
          <div class="service-info flex-grow">
            <div class="flex h-full flex-col justify-between">
              <h1 class="sm:text-4xl text-3xl font-black ">lokadwaya</h1>
              <p class="text-white-primary font-light text-sm">
                Lokadwaya is a platformer game that teaches players about Javanese script. Lokadwaya was created for the Gemastik competition.
              </p>
            </div>
          </div>
          <div class="service-img">
            <img src={Lokadwaya} alt="">
          </div>
        </div>

        <div class="service">
          <div class="service-info flex-grow">
            <div class="flex h-full flex-col justify-between">
              <h1 class="sm:text-4xl text-3xl font-black ">spotless</h1>
              <p class="text-white-primary font-light text-sm">
                Spotless is a website intended for the company profile of a laundry business.  Ocean one was made for the final project of the web development course.
              </p>
            </div>
          </div>
          <div class="service-img">
            <img src={Spotless} alt="">
          </div>
        </div>


      </section>
      
      <section class="footer bg-zinc-50 text-center text-surface/75 dark:bg-neutral-700 dark:text-white/75 lg:text-left">
        <div
          class="flex items-center justify-center border-b-2 border-neutral-200 p-6 dark:border-white/10 lg:justify-between">
          <div class="me-12 hidden lg:block">
            <span>Get connected with me on social networks:</span>
          </div>
          <div class="flex justify-center mx-3">
            <a href="https://www.linkedin.com/in/fairlyardasa/" class="me-6 [&>svg]:h-4 [&>svg]:w-4">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 448 512">
                <path
                  d="M100.3 448H7.4V148.9h92.9zM53.8 108.1C24.1 108.1 0 83.5 0 53.8a53.8 53.8 0 0 1 107.6 0c0 29.7-24.1 54.3-53.8 54.3zM447.9 448h-92.7V302.4c0-34.7-.7-79.2-48.3-79.2-48.3 0-55.7 37.7-55.7 76.7V448h-92.8V148.9h89.1v40.8h1.3c12.4-23.5 42.7-48.3 87.9-48.3 94 0 111.3 61.9 111.3 142.3V448z" />
              </svg>
            </a>
            <a href="https://github.com/fairlyardasa" class="[&>svg]:h-4 [&>svg]:w-4">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                fill="currentColor"
                viewBox="0 0 496 512">
                <path
                  d="M165.9 397.4c0 2-2.3 3.6-5.2 3.6-3.3 .3-5.6-1.3-5.6-3.6 0-2 2.3-3.6 5.2-3.6 3-.3 5.6 1.3 5.6 3.6zm-31.1-4.5c-.7 2 1.3 4.3 4.3 4.9 2.6 1 5.6 0 6.2-2s-1.3-4.3-4.3-5.2c-2.6-.7-5.5 .3-6.2 2.3zm44.2-1.7c-2.9 .7-4.9 2.6-4.6 4.9 .3 2 2.9 3.3 5.9 2.6 2.9-.7 4.9-2.6 4.6-4.6-.3-1.9-3-3.2-5.9-2.9zM244.8 8C106.1 8 0 113.3 0 252c0 110.9 69.8 205.8 169.5 239.2 12.8 2.3 17.3-5.6 17.3-12.1 0-6.2-.3-40.4-.3-61.4 0 0-70 15-84.7-29.8 0 0-11.4-29.1-27.8-36.6 0 0-22.9-15.7 1.6-15.4 0 0 24.9 2 38.6 25.8 21.9 38.6 58.6 27.5 72.9 20.9 2.3-16 8.8-27.1 16-33.7-55.9-6.2-112.3-14.3-112.3-110.5 0-27.5 7.6-41.3 23.6-58.9-2.6-6.5-11.1-33.3 2.6-67.9 20.9-6.5 69 27 69 27 20-5.6 41.5-8.5 62.8-8.5s42.8 2.9 62.8 8.5c0 0 48.1-33.6 69-27 13.7 34.7 5.2 61.4 2.6 67.9 16 17.7 25.8 31.5 25.8 58.9 0 96.5-58.9 104.2-114.8 110.5 9.2 7.9 17 22.9 17 46.4 0 33.7-.3 75.4-.3 83.6 0 6.5 4.6 14.4 17.3 12.1C428.2 457.8 496 362.9 496 252 496 113.3 383.5 8 244.8 8zM97.2 352.9c-1.3 1-1 3.3 .7 5.2 1.6 1.6 3.9 2.3 5.2 1 1.3-1 1-3.3-.7-5.2-1.6-1.6-3.9-2.3-5.2-1zm-10.8-8.1c-.7 1.3 .3 2.9 2.3 3.9 1.6 1 3.6 .7 4.3-.7 .7-1.3-.3-2.9-2.3-3.9-2-.6-3.6-.3-4.3 .7zm32.4 35.6c-1.6 1.3-1 4.3 1.3 6.2 2.3 2.3 5.2 2.6 6.5 1 1.3-1.3 .7-4.3-1.3-6.2-2.2-2.3-5.2-2.6-6.5-1zm-11.4-14.7c-1.6 1-1.6 3.6 0 5.9 1.6 2.3 4.3 3.3 5.6 2.3 1.6-1.3 1.6-3.9 0-6.2-1.4-2.3-4-3.3-5.6-2z" />
              </svg>
            </a>
          </div>
        </div>

        
        <div class="mx-6 py-10 text-center md:text-left">
          <div class="grid-1 grid gap-8 md:grid-cols-2 lg:grid-cols-4">
            <div class="">
              <h6
                class="mb-4 flex items-center justify-center font-semibold uppercase md:justify-start">
                <span class="me-3 [&>svg]:h-4 [&>svg]:w-4">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="currentColor">
                    <path
                      d="M12.378 1.602a.75.75 0 00-.756 0L3 6.632l9 5.25 9-5.25-8.622-5.03zM21.75 7.93l-9 5.25v9l8.628-5.032a.75.75 0 00.372-.648V7.93zM11.25 22.18v-9l-9-5.25v8.57a.75.75 0 00.372.648l8.628 5.033z" />
                  </svg>
                </span>
                Fairly Ardasa
              </h6>
              <p>
                Build using Sveltekit and Tailwind.
              </p>
            </div>
            <div>
            </div>

            <div>

            </div>
            <div>
              <h6
                class="mb-4 flex justify-center font-semibold uppercase md:justify-start">
                Contact
              </h6>
              <p class="mb-4 flex items-center justify-center md:justify-start">
                <span class="me-3 [&>svg]:h-5 [&>svg]:w-5">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="currentColor">
                    <path
                      d="M11.47 3.84a.75.75 0 011.06 0l8.69 8.69a.75.75 0 101.06-1.06l-8.689-8.69a2.25 2.25 0 00-3.182 0l-8.69 8.69a.75.75 0 001.061 1.06l8.69-8.69z" />
                    <path
                      d="M12 5.432l8.159 8.159c.03.03.06.058.091.086v6.198c0 1.035-.84 1.875-1.875 1.875H15a.75.75 0 01-.75-.75v-4.5a.75.75 0 00-.75-.75h-3a.75.75 0 00-.75.75V21a.75.75 0 01-.75.75H5.625a1.875 1.875 0 01-1.875-1.875v-6.198a2.29 2.29 0 00.091-.086L12 5.43z" />
                  </svg>
                </span>
                Sariharjo, Sleman Regency, Special Region of Yogyakarta 
              </p>
              <p class="mb-4 flex items-center justify-center md:justify-start">
                <span class="me-3 [&>svg]:h-5 [&>svg]:w-5">
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 24 24"
                    fill="currentColor">
                    <path
                      d="M1.5 8.67v8.58a3 3 0 003 3h15a3 3 0 003-3V8.67l-8.928 5.493a3 3 0 01-3.144 0L1.5 8.67z" />
                    <path
                      d="M22.5 6.908V6.75a3 3 0 00-3-3h-15a3 3 0 00-3 3v.158l9.714 5.978a1.5 1.5 0 001.572 0L22.5 6.908z" />
                  </svg>
                </span>
                fairlyardasa@mail.ugm.ac.id
              </p>
            </div>
          </div>
        </div>

        <!--Copyright section-->
        <div class="bg-black/5 p-6 text-center">
          <span>© 2024 Copyright: <span class="font-semibold">Fairly Ardasa</span></span>
        </div>
      </section>
    </section>
  </div>
</section>

  