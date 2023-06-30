# spl-6x09 

A simple programming language for 6809 based machines with
Forth-like syntax. 

SPL-6x09 is a Forth-style concatenative stack language. The compiler
is (currently) written in Python and emits 6809/6309 assembly code. 

Originally created by Ron Kneusel for the Apple II (original source
https://home.comcast.net/~oneelkruns/), adapted for the Atari 8bit and
enhanced by Carsten Strotmann (cas@strotmann.de). This 6809/6309
port is based upon the Carsten Strotmann version, found here: 

https://github.com/cstrotm/spl-6502

I will eventually retarget to the HD6309 CPU because of its more rich
instruction set and (albiet limited) support for 32b quantities. 

A significant change from Carsten Strotmann version is that I have 
added the ability to specify some of the primitiives to compile
as inline code. This is particularly useful on the 6809/6309 CPU
with its second User stack, and excellent support of 16b data. It
just didn't make much sense to have so many "JSR" calls to many 
of the primitives after I realized that they reduced to a very 
few 6809 instructions - even moreso for the 6309.

