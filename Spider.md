# Spider

## 1. Open the Developer Tools

Locate the Universal Selector, then choose Copy → Copy selector.

## 2. Open the Console

Run the following code to verify the main content area:

```js
document.querySelectorAll(
  "#root > div > main > div > div.Topstory-container > div.Topstory-mainColumn"
).length
```

Expected result: `1`, which confirms the main content area is unique and stable.  

Directly print link data:

```
 [...mainColumn.querySelectorAll("a")]
  .map(a => ({
    title: a.innerText.trim(),
    href: a.href
  }))
  .filter(x => x.title.length > 5)
  .slice(0, 10);
```

## 3. Use AI to Complete the Playwright Code

Generate Playwright scripts for login initialization and web scraping.

## 4. Create a Working Directory

Place and run the login initialization script, log in manually once (the login state will be saved for future use), then run the scraping script.
