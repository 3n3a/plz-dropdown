<script lang="ts">
  import AutoComplete from 'simple-svelte-autocomplete'

  const loadSuggestions = async (query: string, limit: number) => {
    const options = {
      method: "GET",
      mode: "cors",
      credentials: "include",
      headers: {
        "apikey": "uEzad5RVG9e9967xypBS8sFzKRadEtCV",
        "accept": "application/json"
      },
    }
    const res = await fetch(`https://api.3n3a.ch/plz/search?q=${query}`, options)
    const data = await res.json()
    return data
  }

</script>

<AutoComplete
  searchFunction={loadSuggestions}
  showLoadingIndicator={true}

  labelFunction={item => item ? item.postal_code + ' ' + item.place : ''}
/>