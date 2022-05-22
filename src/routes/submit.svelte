<script>
import Notice from "../components/Notice.svelte";
</script>
<svelte:head>
    <script src="https://static.airtable.com/js/embed/embed_snippet_v1.js"></script>
</svelte:head>
<Notice showLink={false}/>
<iframe 
    class="airtable-embed airtable-dynamic-height" 
    src="https://airtable.com/embed/shrTI5MHC1E7JJJSb?backgroundColor=red" 
    frameborder="0" onmousewheel="" 
    width="100%" height="2231" 
    style="background: transparent; border: 1px solid #ccc;" 
    title="form">
</iframe>