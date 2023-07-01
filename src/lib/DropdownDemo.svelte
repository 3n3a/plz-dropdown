<script lang="ts">
  import AutoComplete from 'simple-svelte-autocomplete'

  const loadSuggestions = async (query: string, limit: number) => {
    const res = await fetch(`https://plz.enea.tech/api/plz/search?q=${query}`)
    const data = await res.json()
    return data
  }

</script>

<AutoComplete
  searchFunction={loadSuggestions}
  showLoadingIndicator={true}

  labelFunction={item => item ? item.postal_code + ' ' + item.place : ''}
/>