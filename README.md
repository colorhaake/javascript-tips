# Javascript Tips
Useful javascript tips and code snippet

## extract url query string by regular expression
```
const extractUrlValue = (key, url) => {
  // 1. character before '${key}=' would be '?' or '&'
  // 2. find '${key}='
  // 3. match strings until '&'
  const match = url.match('[?&]' + key + '=([^&]+)')
  return match ? match[1] : null
}
```

Example:
```
  const key = 'v'
  const url = 'https://www.youtube.com/watch?v=SBOVkptjJhE'

  // SBOVkptjJhE
  console.log(extractUrlValue(key, url))

```

