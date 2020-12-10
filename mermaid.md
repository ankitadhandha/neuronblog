### Mermaid-js

<details><summary>mermaid-js</summary>

```html
<script src="https://cdn.jsdelivr.net/npm/mermaid/dist/mermaid.min.js"></script>
<script>
window.addEventListener("load", mermaid.initialize({startOnLoad:true}))
</script>
```
</details>

```{.mermaid}
sequenceDiagram
    Alice->>John: Hello John, how are you?
    activate John
    John-->>Alice: Great!
    deactivate John
```

~~~markdown
```{.mermaid}
sequenceDiagram
    Alice->>John: Hello John, how are you?
    activate John
    John-->>Alice: Great!
    deactivate John
```
~~~
