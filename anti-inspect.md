Description:

`can you find the answer? WARNING: do not open the link your computer will not enjoy it much. URL: http://litctf.org:31779/ Hint: If your flag does not work, think about how to style the output of console.log`

Opening the link in a browser might not be a good idea, as it might hang the browser (this happened in my case).

So a better approach will be to use `curl` to get the HTML response.

```
$ curl http://litctf.org:31779/
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <script>
      const flag = "LITCTF{your_%cfOund_teh_fI@g_94932}";
      while (true)
        console.log(
          flag,
          "background-color: darkblue; color: white; font-style: italic; border: 5px solid hotpink; font-size: 2em;"
        );
    </script>
  </body>
</html>
```

We can see the flag there. However, submitting the shown flag will prompt the flag to be incorrect.

The hint in the description states: `, think about how to style the output of console.log`

A Google search will tell that `%c` is used for styling.
```
const style = 'background-color: darkblue; color: white; font-style: italic; border: 5px solid hotpink; font-size: 2em;'
console.log("%cHooray", style);
```

(taken from https://developer.chrome.com/docs/devtools/console/format-style)

So the correct flag would be: `LITCTF{your_fOund_teh_fI@g_94932}`
