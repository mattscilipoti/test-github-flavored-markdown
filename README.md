# test-github-flavored-markdown
Test various formatting options for GFM

## Recommended

## Show/Hide w/markdown (needs proper indentation)

<details class="qa">
  <summary class="question">
    **Q**. How do we format lists and code as summary/details?
    Note: indentation matters (markdown processing stopped when indenting within blockquote tab level.
  </summary>
  <blockquote>
  ```js
  console.log("It works!"); // note: markdown indentation matters
  ```

  And the list?
  - item 1
  - item 2
  - item 3
  </blockquote>
</details>

# Tests

## Show/Hide w/ code snippet

### Indentation examples

#### Works!

<details class="qa">
  <summary class="question">
    **Q**. Code syntax: plain, level
  </summary>
  ```js
  console.log("a");
  ```
</details>

<details class="qa">
  <summary class="question">
    **Q**. Code syntax: plain, outdented
  </summary>
```js
console.log("a");
```
</details>

<details class="qa">
  <summary class="question">
    **Q**. Code syntax: within blockquote. WORKS! (When indentation is correct)
  </summary>
  <blockquote class="answer">
  ```js
  console.log("a");
  ```
  </blockquote>
</details>


<details class="qa">
  <summary class="question">
    **Q**. Code syntax: wihtin div
  </summary>
  <div>
  ```js
  console.log("a");
  ```
  </div>
</details>

#### Fail!

<details class="qa">
  <summary class="question">
    **Q**. Code syntax: plain, indented (which "looks" like proper indentation, but is not processed as markdown
  </summary>
    ```js
    console.log("a");
    ```
</details>


<details class="qa">
  <summary class="question">
    **Q**. Code syntax: div with blockquote
  </summary>
  <div class="answer">
    <blockquote>
    ```js
    console.log("a");
    ```
    </blockquote>
  </div>
</details>

## Show/Hide w/ markdown list

<details class="qa">
  <summary class="question">
    **Q**. list, bare
  </summary>
I see five:

- font color
- first character
  - background-color
  - border-color
  - box-shadow
- background
</details>

<details class="qa">
  <summary class="question">
    **Q**. list, in blockquote
  </summary>
  <blockquote>
I see five:
- font color
- first character
  - background-color
  - border-color
  - box-shadow
- background
  </blockquote>
</details>

<details class="qa">
  <summary class="question">
    **Q**. list, indented within blockquote
  </summary>
  <blockquote>
    I see five:
    - font color
    - first character
      - background-color
      - border-color
      - box-shadow
    - background
  </blockquote>
</details>


<details class="qa">
  <summary class="question">
    **Q**. list: give up and use "pre"
  </summary>
  <pre>
I see five:
- font color
- first character
  - background-color
  - border-color
  - box-shadow
- background
  </pre>
</details>
