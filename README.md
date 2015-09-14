# ndebug

Purpose
-------

This is a repo and workflow for a simple ES6/Node.js/Lodash scratchpad. I got tired of writing bits of code in the
web inspector, since it's really difficult to go back and edit code. I wanted a quick little thing I could open up
and immediately start writing some ES6 code that also has Lodash available.

Installation
------------

1. Create a file in the root of this directory named `ndebug.js`. This is your scratchpad.
2. Run `npm install`.
3. Use Vim.
4. Install [sjl](https://github.com/sjl/)'s [Clam.vim](https://github.com/sjl/clam.vim). Thanks, Steve!
5. Stick this (or something like it) in your [`.vimrc`](https://github.com/nicksergeant/dotfiles/blob/ac16349a064ad626e37ea4b95c4dac729cf6ed0c/vimrc#L106):

`au BufWritePost ndebug.js execute "normal! :Clam npm run build\<cr>"`

Usage
-----

I map `d` (for "debug") in my [Fish config](https://github.com/nicksergeant/dotfiles/blob/master/config.fish#L148-L150),
and whenever I save the scratchpad (ndebug.js), a buffer updates with the result of running through Babel/Node. The
buffer remains until I close it, and it'll update each time I save the scratchpad, without losing focus of the
scratchpad buffer:

![http://i.nick.sg/image/2i2N2E1B0j25/gif.gif](http://i.nick.sg/image/2i2N2E1B0j25/gif.gif)
