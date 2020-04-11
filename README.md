# debounce-hook
simple  hook for debounce


### usage

```js
import useDebounce from 'use-debounce'
let [query, setQuery] = React.useState('')
let debouncedQuery = useDebounce(query, 500)
    useEffect(()=> {
    if(debouncedQuery){
      makeQuery(debouncedQuery)
      .then((res)=> {
        setResults(res)
      })
    } else {
      setResults([])
    }
  },[debouncedQuery])


  return(
     <div>
      <input
          value={query}
          placeholder='Search...'
          onChange={e => setQuery(e.target.value)}
        />
      <div>
  )

```
