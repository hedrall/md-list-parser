# md-list-parser

This is a simple parser for Markdown list.

[live demo](https://hedrall.github.io/md-list-parser/)

# install

`npm install md-to-github-issues`

# how to use (example)

```ts
import * as LP from 'md-list-parser';
const input = `
- a
  - b
  - d
    - e
- f
`;

const result = LP.parse(input);
```

to get 
```ts
const result = [
    {
        title: 'a',
        children: [
            {
                title: 'b',
            },
            {
                title: 'd',
                children: [
                    {
                        title: 'e',
                    },
                ],
            },
        ],
    },
    {
        title: 'f',
    },
]
```
