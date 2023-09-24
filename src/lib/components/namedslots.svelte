<script>

</script>
<body>
    <div class="card max-w-md w-full bg-white shadow-lg rounded-lg overflow-hidden">
        <div class="card-header">
            <slot name="header">

            </slot>
        </div>
        <div class="card-content">
            <slot name="content">

            </slot>
        </div>
        {#if $$slots.footer}
        <div class="card-footer">
            <slot name="footer">

            </slot>
        </div>
        {/if}
    </div>
</body>