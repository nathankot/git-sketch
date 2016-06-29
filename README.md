<img src="https://raw.githubusercontent.com/nathankot/git-sketch/master/logo.png" width="150" height="150" />

# git-sketch

_Better diffs for your Sketch files._

Go from this:

```diff
diff --git a/fixture.sketch b/fixture.sketch
index c5b1e42..838b58a 100644
Binary files a/fixture.sketch and b/fixture.sketch differ
```

To this:

```diff
diff --git a/fixture.sketch b/fixture.sketch
index c5b1e42..838b58a 100644
--- a/fixture.sketch
+++ b/fixture.sketch
@@ -442,7 +442,7 @@
     {
       "id" : "9610356C-A043-45BD-8E93-08DC0E5DBBB0",
       "name" : "Page 3",
-      "bounds" : "-142.000000,-104.000000,386.000000,386.000000",
+      "bounds" : "-142.000000,-104.000000,771.000000,386.000000",
       "layers" : [
```

## Installation

Download `git-sketch` and put it somewhere in your `PATH`, ensure that it has
`u+x` persmission, you could run this if you trust me:

```sh
curl https://raw.githubusercontent.com/nathankot/git-sketch/master/git-sketch \
  -o /usr/local/bin/git-sketch
chmod u+x /usr/local/bin/git-sketch
```

Setup the `sketch` filter for git, globally:

```sh
git config --global diff.sketch.textconv git-sketch
```

Add the following to your local or global `.gitattributes` file:

```
*.sketch filter=sketch diff=sketch
```

Enjoy :)

## License

> Copyright (c) 2016  Nathan Kot
>
>
> Permission is hereby granted, free of charge, to any person obtaining a copy of
> this software and associated documentation files (the "Software"), to deal in
> the Software without restriction, including without limitation the rights to
> use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
> the Software, and to permit persons to whom the Software is furnished to do so,
> subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in all
> copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
> IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
> FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
> COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
> IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
> CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
