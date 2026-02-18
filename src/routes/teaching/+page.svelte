<script>
    import Locandina from '$lib/assets/LocandinaIndirizzo.pdf'
    import PdfViewer from 'svelte-pdf';
</script>

<div style="width: 80%; margin: auto">
    <PdfViewer url={Locandina} />
</div>