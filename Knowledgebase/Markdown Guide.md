A basic guide to the Markdown Language.

```
NOTE:

Some of the markdown outcomes in this guide won't show on the website, as not all websites support all types of markdown. You have to be experimental with what you try and don't try.
```

---

### Bolding Text

To bold text we use `**` around our text

Example: `**nice**`
Outcome: **nice**

---

### Underlining Text

To underline text we use `__` around our text

Example: `__nice__`
Outcome: __nice__

---

### Cross-out Text

To cross-out text we use `~~` around our text

Example: `~~nice~~`
Outcome: ~~nice~~

---

### Italicize Text

To italicize text we use `*` around our text

Example: `*nice*`
Outcome: *nice*

---
---

### Text Headers

Their are 4 types of headers for your MD Document.

We define header sizes with a `#`

---

Example: `# Header Size One`

Outcome:
# Header Size One

---

Example: `## Header Size Two`

Outcome:
## Header Size Two

---

Example: `### Header Size Three`

Outcome:
### Header Size Three

---

Example: `#### Header Size Four`

Outcome:
#### Header Size Four

---
---

### Dividers

To create a divider we use `---` by itself.

Example: `---`
Outcome:

---

^ Divider

---

### Hyperlinks

To create a hyperlink we use `[text](https://text.com)`

Example: `[@Hyperz](https://hyperz.net/)`
Outcome: [@Hyperz](https://hyperz.net/)

---

### Spoiler Text

To create a spoiler we use `||` around our text.

Example: `||Bruh Rick Astley||`
Outcome: ||Bruh Rick Astley||

---

### Code Blocks

To create a code block we use **```** at the top **AND** bottom lines of our code.

An example of this would be like:

```
some code here
```

OR

We can use code blocks with a dedicated coding language involved by adding a code language after the top bar of the code block like this:

```js
const bruh = require('discord.js');
```

With code blocks it supports multiple lines as-well. So you can write a whole file just like this directly in code-block form:

```js

const freeCringeLol = require('discord.js')
const client = new freeCringeLol.Client()

client.on('ready', ready => {
  console.log(`I am ready papi`)
  client.user.setPresence({
    activity: {
      name: "Bruh Cringe",
      type: "WATCHING"
    },
    status: "dnd"
  });
});

client.on('guildMemberAdd', u => {
  let chan = client.channels.cache.get('YOUR WELCOME CHANNEL ID')
  chan.send(`Welcome, ` + `ã€ŒBIA:hearts:+ã€${u.tag}` + ` to the server!`)
});

client.login(`Your Token`)

```

The external piece of this code block looks like this:

![](https://cdn.hyperz.net/tb2hlgka.png)

---

### Embed Images

To embed an image into your markdown file, we use `![]()`

This is very similar to our hyperlink documentation, but with an `!`

Example: `![](https://cdn.dribbble.com/users/1216710/screenshots/4463006/frame-_000000-000179_.gif)`
Outcome:

![](https://cdn.dribbble.com/users/1216710/screenshots/4463006/frame-_000000-000179_.gif)

---

### Borders

In markdown for borders we use `> `

Example:

```md
> **Hotel Hyperz**
> By [@Hyperz](https://hyperz.net/discord)
```

Outcome:

![](https://cdn.hyperz.net/pxxn7u1w.png)

---

### Checkboxes

Yes, you can do checkboxes in markdown... These are hard to explain, so you can just explore these more on your own.

Example / Outcome:

```md
[ ] This is cool
[X] This is even cooler
```

![](https://cdn.hyperz.net/qm5aqxfh.png)

---

### Tables

Really I cannot be bothered explaining this one, just take this example and try working it out on your own :]

**Example:**

```md
| Task           | Time required | Assigned to   | Current Status | Finished | 
|----------------|---------------|---------------|----------------|-----------|
| Calendar Cache | > 5 hours  |  | in progress | - [x] ok?
| Object Cache   | > 5 hours  |  | in progress | [x] item1<br/>[ ] item2
| Object Cache   | > 5 hours  |  | in progress | <ul><li>- [x] item1</li><li>- [ ] item2</li></ul>
| Object Cache   | > 5 hours  |  | in progress | <ul><li>[x] item1</li><li>[ ] item2</li></ul>
```

**Outcome:**

| Task           | Time required | Assigned to   | Current Status | Finished | 
|----------------|---------------|---------------|----------------|-----------|
| Calendar Cache | > 5 hours  |  | in progress | - [x] ok?
| Object Cache   | > 5 hours  |  | in progress | [x] item1<br/>[ ] item2
| Object Cache   | > 5 hours  |  | in progress | <ul><li>- [x] item1</li><li>- [ ] item2</li></ul>
| Object Cache   | > 5 hours  |  | in progress | <ul><li>[x] item1</li><li>[ ] item2</li></ul>
