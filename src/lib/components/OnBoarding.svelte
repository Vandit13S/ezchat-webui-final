<script>
import { getContext } from 'svelte';
const i18n = getContext('i18n');

//import { WEBUI_BASE_URL } from '$lib/constants';
    import {goto} from '$app/navigation';
//import Marquee from './common/Marquee.svelte';
//import SlideShow from './common/SlideShow.svelte';
import ArrowRightCircle from './icons/ArrowRightCircle.svelte';

export let show = true;
export let getStartedHandler = () => {
        //navigate to the auth page
        goto('/auth')
    };
</script>

{#if show}
<div class="w-full h-screen bg-black relative">
<div class="w-full h-screen max-h-[100dvh] text-white relative">
<div class="fixed m-10 z-50">
<div class="flex space-x-2">
<div class=" self-center">
<!--<img
crossorigin="anonymous"
src="{WEBUI_BASE_URL}/static/favicon.png"
class=" w-6 rounded-full"
alt="logo"
/>-->
                    <img
crossorigin="anonymous"
src="static\favicon.png"
class=" w-6 rounded-full"
alt="logo"
/>
</div>
</div>
</div>
        <!-- Black Background -->
    <div class="w-full h-screen bg-black relative">
        <div class="w-full h-screen max-h-[100dvh] text-white relative">
            <!-- SlideShow Component -->
            <!-- <SlideShow duration={5000} /> -->

            <!-- Gradient Overlay -->
            <div
                class="w-full h-full absolute top-0 left-0 bg-gradient-to-t from-black via-transparent to-transparent"
            ></div>

            <!-- Backdrop Blur -->
            <div class="w-full h-full absolute top-0 left-0 backdrop-blur-sm bg-black/50"></div>

            <!-- Centered Text -->
            <div class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 text-center">
                <div class="text-white text-5xl font-bold">Welcome to EZChat</div>
                <div class="text-white text-2xl mt-2">created by - EZ Tech</div>
            </div>

            <!-- Button -->
            <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 flex flex-col justify-center items-center">
                <button
                    class="relative z-20 flex p-3 rounded-full bg-white/10 hover:bg-white/20 transition font-medium text-sm"
                    on:click={() => {
                        getStartedHandler();
                    }}
                >
                    <ArrowRightCircle className="w-6 h-6" />
                </button>
                <div class="mt-1.5 font-primary text-base text-white font-medium">Get Started</div>
            </div>
        </div>
    </div>
    </div>
</div>
{/if}