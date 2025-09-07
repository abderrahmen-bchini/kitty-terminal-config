# kitty-terminal-config

I thought it would be helpful to share my terminal configuration, especially since it took me three months to get to this result (I'm new to this).

## `kitty.conf`

I’ve attached my `kitty.conf` file in this repo. All you have to do is copy it and paste it into your `~/.config/kitty/kitty.conf`. But don’t forget to create a backup of your original file—you may need it in the future.

## ASCII Art & Neofetch on Startup

You can enable this by adding the following lines to your `.bashrc` file:

```bash
cat ~/ascii_art.txt
neofetch
```

*Note*: `ascii_art.txt` should contain ASCII art, which you can easily get from [asciiart.eu](http://asciiart.eu/).

## Custom Neofetch ASCII Art

1. Open `~/.config/neofetch/config.conf`.
2. Scroll down to `#image_backend` and change its value to:

   ```bash
   image_backend="ascii"
   ```

   *(Remove the `#` to uncomment it.)*
3. Set `image_source` to the path of your ASCII art `.txt` file. You can find cool art online or create your own by converting an image to ASCII art (again, see [asciiart.eu](http://asciiart.eu/)).

*Note*: You can change the color of the ASCII art using escape codes. For example, use `\033[30m` for black and end it with `\e[0m` to reset the color.

Here’s a table of available colors:

| Code  | Color         | Foreground Escape Code        | Background Escape Code          |
| ----- | ------------- | ----------------------------- | ------------------------------- |
| 30    | Black         | `\033[30m`                    | `\033[40m`                      |
| 31    | Red           | `\033[31m`                    | `\033[41m`                      |
| 32    | Green         | `\033[32m`                    | `\033[42m`                      |
| 33    | Yellow        | `\033[33m`                    | `\033[43m`                      |
| 34    | Blue          | `\033[34m`                    | `\033[44m`                      |
| 35    | Magenta       | `\033[35m`                    | `\033[45m`                      |
| 36    | Cyan          | `\033[36m`                    | `\033[46m`                      |
| 37    | White         | `\033[37m`                    | `\033[47m`                      |
| 90–97 | Bright Colors | `\033[9xm` (e.g., `\033[91m`) | `\033[10xm` (e.g., `\033[101m`) |
