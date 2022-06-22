<script lang="ts">
    import Youtube from "svelte-youtube-embed";
    export let max = 100;

    const videos =[
        "0mnBCWeBHog",
        "Yb5u36PJKwI",
        "yUcNXZt9gRI",
        "IL8LhUVejZw",
        "mIAmMnLx7bA",
        "6i2qvZ61BkM"
        ];

    let sliced = videos.slice(0,max);
</script>
<a href="/videos" class=" block m-auto rounded text-blue-500 text-center text-xl py-4" >הקלטות אחרונות</a>
<div class=" md:flex w-auto text-center justify-center px-6 h-auto flex-wrap md:m-auto md:w-4/5 ">
   {#each sliced as vid}
   <div class="w-auto md:w-64 block md:px-2 md:py-1 ">
        <Youtube id={vid}/>
   </div>
   {/each} 
</div>