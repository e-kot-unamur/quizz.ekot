<script>
    export let justification;
    export let goodAnswer;
</script>

<style>
    .justification {
        max-height: 100px;
        overflow-y: auto;
        scrollbar-width: thin;
    }

    .success {
        background-color: #6AD47D;
    }
</style>


{#if justification != "" && goodAnswer} 
    <div class="alert success mt-3 justification" role="alert">
        {justification}
    </div>
{:else if justification != ""} 
    <div class="alert alert-danger mt-3 justification" role="alert">
        {justification}
    </div>
{/if}





