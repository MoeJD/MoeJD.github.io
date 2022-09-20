## Blog Post Title From First Header

Due to a plugin called `jekyll-titles-from-headings` which is supported by GitHub Pages by default. The above header (in the markdown file) will be automatically used as the pages title.

If the file does not start with a header, then the post title will be derived from the filename.

This is a sample blog post. You can talk about all sorts of fun things here.

---

### This is a header

#### Some T-SQL Code

```tsql
SELECT This, [Is], A, Code, Block -- Using SSMS style syntax highlighting
    , REVERSE('abc')
FROM dbo.SomeTable s
    CROSS JOIN dbo.OtherTable o;
```

#### Some PowerShell Code

```powershell
Write-Host "This is a powershell Code block";

# There are many other languages you can use, but the style has to be loaded first

ForEach ($thing in $things) {
    Write-Output "It highlights it using the GitHub style"
}
```
![d094457dba93724d931a192ec26334106a953a55ee59ea7f063499695f220cb2](https://user-images.githubusercontent.com/76531825/191363143-41bb096b-27b5-4f06-b930-595f655ef98e.png)

```python
# https://stackoverflow.com/questions/3463930/how-to-round-the-minute-of-a-datetime-object
def dt_time_mod(time, delta, epoch=None):
    if epoch is None:
        epoch = datetime(1970, 1, 1, tzinfo=time.tzinfo)
    return (time - epoch) % delta


def dt_time_round(time, delta, epoch=None):
    mod = dt_time_mod(time, delta, epoch)
    if mod < delta / 2:
        return time - mod
    return time + (delta - mod)


def dt_time_floor(time, delta, epoch=None):
    mod = dt_time_mod(time, delta, epoch)
    return time - mod


def dt_time_ceil(time, delta, epoch=None):
    mod = dt_time_mod(time, delta, epoch)
    if mod:
        return time + (delta - mod)
    return time


def dt_timedelta_to_time(dt_td: timedelta):
    return (datetime.min + dt_td).time()
```
