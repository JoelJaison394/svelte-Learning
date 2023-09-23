<script>
    import Inner from './inner.svelte';
</script>

<body>
    <!-- now we are acessesing the greet event fom the inner compt  and since we are not handling of the event it will automatically forwarded into parent component-->  
    <Inner on:greet/>   
</body>
