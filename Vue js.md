rfc = request for comments

es una forma que se mandan nueva funcionalidades a los usuarios para que ellos den feed back y ver si se pone definitivamenrte en el framework


# Motivation

[](https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md#motivation)

This proposal's main goal is reducing the verbosity of Composition API usage inside Single File Components (SFCs) by directly exposing the context of `<script setup>` to the template.

We have a prior proposal for `<script setup>` [here](https://github.com/vuejs/rfcs/blob/sfc-improvements/active-rfcs/0000-sfc-script-setup.md), which is currently implemented (but marked as experimental). The old proposal opted for the `export` syntax so that the code would play well with unused variable checks.

This proposal takes a different direction based on the premise that we can offer customized linter rules in `eslint-plugin-vue`. This allows us to aim for the most succinct syntax possible.



**`defineProps`:**

- Para definir propiedades que un componente puede recibir.
-<script setup lang="ts"> defineProps<{ msg: string }>(); </script>

**`defineEmits`:**

- Para declarar los eventos que el componente puede emitir.
- <script setup lang="ts"> defineEmits<{ (event: 'increment', value: number): void }>(); </script>

### Top level await

[](https://github.com/vuejs/rfcs/blob/master/active-rfcs/0040-script-setup.md#top-level-await)

Top level `await` can be used inside `<script setup>`. The resulting `setup()` function will be made `async`:

<script setup>
  const post = await fetch(`/api/post/1`).then((r) => r.json())
</script>


v-html = The double mustaches interpret the data as plain text, not HTML. In order to output real HTML, you will need to use the [`v-html` directive](https://vuejs.org/api/built-in-directives.html#v-html):


```
<p>Using text interpolation: {{ rawHtml }}</p>
<p>Using v-html directive: <span v-html="rawHtml"></span></p>
```

