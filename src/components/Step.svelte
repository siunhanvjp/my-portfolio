<script>
    export let step; // include github repo
</script>

<div
    class="p-4 sm:p-6 md:p-8 flex flex-col gap-4 rounded-lg border border-solid border-violet-700 text-center group hover:border-violet-400 duration-200"
>
    <div
        class="bg-slate-950 grid place-items-center px-4 text-5xl md:text-6xl -mt-10 sm:-mt-12 md:-mt-14 lg:-mt-16 mx-auto duration-200"
    >
        <!-- <i class={step.icon} /> -->
        <div class="relative shadow-2xl grid place-items-center">
            <img
                src={step.imgSrc}
                alt="Project Images"
                class="object-cover z-[2] max-h-[20vh]"
            />
        </div>
    </div>
    <h3 class="font-medium text-xl sm:text-2xl md:text-3xl">
        {step.name}
    </h3>
    <slot />
    <p>{step.description}</p>
    <div class="flex justify-center space-x-8">
        {#each step.logos as logo}
            <img src={logo.logoSrc} alt={logo.logoName} width="40">
        {/each}
    </div>
    <div class="flex-1 flex justify-between gap-4 items-end">
        {#if step.github === ""}
            <span class="cursor-not-allowed opacity-50 hover:opacity-50">
                <i class="fa-brands fa-github fa-xl"></i>
            </span>
        {:else}
            <a target="_blank"
                href={step.github}
                class="hover:scale-150">
                <i class="fa-brands fa-github fa-xl fa-bounce"></i>
            </a>
        {/if}
        

        {#if step.webUrl === ""}
            <div class="cursor-not-allowed opacity-50 hover:opacity-50">
                <span class="z-4 ">
                    Go to &rarr;
                </span>
            </div>
        {:else}
            <div class= "cursor-pointer hover:text-slate-950 duration-200 relative after:absolute after:top-0 after:h-0 after:right-full after:bg-white after:w-full after:h-full after:duration-200 hover:after:translate-x-full after:z-[-1] overflow-hidden">
                <a target="_blank" href={step.webUrl} class="z-4">
                    Go to &rarr;
                </a>
            </div>
        {/if}
    </div>
</div>