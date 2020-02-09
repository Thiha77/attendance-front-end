<script>
    import Api from '../../components/Api.svelte'
</script>

<Api url="http://localhost:5000/users" method="get" let:data let:loading let:error>
{#if data}
<ul>
    {#each data as user}
    <li>{user.name}</li>
    {/each}
</ul>
{:else if loading}
<h1>loading</h1>
{:else if error}
<h1>{error}</h1>
{/if}
</Api>


<style></style>