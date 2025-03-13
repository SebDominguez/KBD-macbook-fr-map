# Kbd French keyboard layout for MacBook

The `mac-fr.map` file is a complete mess. It doesn't even map <kbd>Control</kbd>+<kbd>C</kbd> correctly and uses redundant compose and string definitions that are already implemented in `compose.latin`. and `string`.

For some reason, `mac-fr.map` uses <kbd>AltGr</kbd>+<kbd>E</kbd> for the Euro symbol (€) instead of utilizing the dedicated Euro key, and instead uses the Euro key for the cent symbol.

`mac-fr.map` also mapped <kbd>⌘ Command</kbd> keys for switching TTYs, which is illogical. I've remapped these to <kbd>⌘ Command</kbd> + <kbd>Left</kbd> or <kbd>Right</kbd> to switch between TTYs, which is more intuitive.

Since Mac keyboards generally don't distinguish between <kbd>Alt</kbd> and <kbd>AltGr</kbd> (they have an <kbd>⌥ option</kbd> key instead ), I've mapped both to <kbd>AltGr</kbd> and <kbd>⌘ command</kbd> to <kbd>Alt</kbd>. Therefore all the Meta_keys are mapped to <kbd>⌘ command</kbd>.

E.g.:
- <kbd>⌘ command</kbd>+<kbd>a</kbd> = Meta_a `0x0861`
- <kbd>⌥ option</kbd>+<kbd>a</kbd> = ae `0x00e6`
- <kbd>^ control</kbd>+<kbd>⌘ command</kbd>+<kbd>a</kbd> = Meta_Control_a `0x0801`

If you dislike this behavior, I've commented out sections of the file, making it very easy to edit. ASCII diagrams are also included to assist with key editing.

If you see question mark (?) symbols, don't panic. It's just that the French layout outputs unusual characters, like Greek symbols with AltGr+Shift+Q, which aren't supported in the virtual console (vconsol). However, the output Unicode numbers are correct. I've painstakingly mapped every one of them, except for the Apple logo, which was out of range (it's in the Private Use Area Unicode range). So, I've mapped it to the Compose key.

You can, for example, draw a copyright symbol by pressing <kbd>Compose</kbd> key (wich is <kbd>⌥</kbd>+&) and then typing a left parenthesis `(` followed by the letter `c`.

I've also mapped all the accent keys to their respective dead keys, so pressing '^', for instance, waits for the next letter to be accented."