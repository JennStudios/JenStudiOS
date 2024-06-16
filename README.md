# JenStudiOS
Repository for some of my custom OS files, maybe later a full OS. Due to aseprite I'm not sure how to license this yet. Let's ambiguously say *my* files are open source and I don't know about the others I didn't make


readme.serverVersion
========================================================================
Hello


Welcome to JenStudiOS, the official development environment of 
indie game dev Jen Studios.  This isn't so much a novel OS as bodhi with
lxde and all the tools I use to develop games. 

Please give the Bodhi devs love they work very hard to make an amazing
desktop environment and apps and repository.

This started when I became estranged from Lubuntu after they got rid of 
lxde which, in my opinion, is what made lubuntu great. So now I am
done with Lubuntu. I never thought I'd make a custom ubuntu (I was happy
with lxdelubuntu for a long time) but I guess this is what I have to do)

=======================================================================

JenStudiOS has lxde and moksha. Partly because removing moksha broke 
the install building it with cubic. 

Both are extremely light weight running about 250 mb of ram at idle 
before installing random stuff, both quite good in vm (though you
should only test games in vm, not develop them, due to input lag)

I've also opted to keep the bodhi terminal, Terminology, however both
are included if you prefer the more simplistic lxterminal.

In later versions, after I have the time, I'll move to buiding
up my own version from a headless ubuntu server sort of start. I started
by doing this but then broke the keyrings beyond repair trying to 
install docker. Docker is unnecessarily difficult to install 
if you cannot copy paste the code. 

I hope they will eventually have a mirror on launch pad or some-
-thing. You'll find docker engine already installed here though. 

========================================================================

What is JenStudiOS

JenStudiOS includes all the libraries and tools I use to make video 
games. 

I've included nothing I don't use in some capacity.

Assuming the install of this OS was flawless you will be able to jump
into making games immediately. I've spent countless nights for weeks,
weekends, etc. Hunting down dependencies, libraries, etc trying to just
start to begin to make games or apps. With this you should be setup
without having to configure, compile, run, execute, jump, get 5 degrees
and become a cross country runner JUST to start developing games. 

========================================================================

WHAT ARE THESE "THINGS"?

You'll notice in your /home/ folder that godot 4.x is included which is 
a powerful, light weight, FOSS game engine. 

You'll also find a bash script for docker that compiles Aseprite from 
source. It is against the aseprite EULA for me to include an already
compiled aseprite binary. It is free to compile and use from source  
yourself. THe docker script should compile it for you just by clicking
it. I've also tried to bake as many of the dependencies into the ISO
baseline as I can, so hopefully you don't have any problems with it. 
Aseprite is the premiere pixel art and animation software for 2d games
or general sprite art.

There is a slight problem though. When installing (idr which exactly,
I think emscripten) one of the dependencies needed to compile aseprite 
you'll run into an issue with a nodejs version. The issue is that the 
archive used from emsdk's mirror (when building cutting edge package 
from source) is corrupt and won't let you install it. To make matters
worse it's not obvious or intuitive how to get around this part of the
build/install instructions because the code is not easy to understand
to me. So even if you have the nodejs version needed to do the job 
you won't be able to use it, because the make/build/install script
demands to pull the corrupted mirror. I've gone ahead and used the
version from synaptic, personally, because it's stable and works fine.

If you want to uninstall any of these that's fine. Just open synaptic
and look for these packages or run the apt-get remove and apt purge 
for each in terminal. At the bare minimum all your really need to
make games is: godot4 (included,) lmms+zynth (included,) and 
aseprite (docker script to compile it automatically included and almost
all of the dependencies needed for docker to work.) I cannot share my 
aseprite binary with you directly because it violates the aseprite 
Eula and I don't wanna really be involved in pirating a $20 app that's
free to compile from source. Aseprite is the rare elusive "open source,
free to compile, not free to redistribute" category that almost nothing 
ever made is in. You can compile it or buy a copy off steam, humble bundle,
or itch.io. After you've compiled or bought your  aseprite you can 
uninstall the dependencies needed to compile it. Though they might 
still be useful anyway, because like emsdk will help you convert things
to webgl. So like maybe if you're interested in making browser games 
it could be helpful but I recommend looking into crossbrowdy below if 
you're interested in that as well.


INCLUDED IN JENSTUDIOS:

[SDL2 Dev libs] -- SDL 2 is a potent graphics framework, powers android
				and can be found in an endless number of open source
				software. 			
www.libsdl.org


[Pygame] -- renders images to linux terminal and animates
www.pygame.org


[Pyglet3d] -- Object-oriented application programming interface 
www.pyglet.org


[PyOpenGL] -- Python binding for OpenGL and related APIs
www.pyopengl.sourceforge.net
	
	(Note: you can use pyopengl in your pyglet3d programs and it will
		work, so you can combine the two. You can use pyglet3d, pygame,
		& pyopengl together to make impressive multimedia applicaitons
		Allowing you to work at a high level, low level, or somewhere
		inbetween!)


[Cross Browdy] --  Multimedia Jscript Framework used to make emulators
				engines, etc. Works with browsers, phones, pcs, etc.
www.crossbrowdy.com


[Geany] -- powerful, light weight gtk based ide, supplimental for 
		notepad++. Kate is a good alternative but i wanted to avoid as
		much gnome and kde software as possible. Feel free to choose 
		another editor with text highlights.
www.geany.org
	
	(Note: I've included a GoDot plugin for geany which will include
	instructions for how to set it up)


[GoDot] -- Very powerful FOSS engine for making games for all platforms
www.godotengine.com


[Freetype 2] -- Font rendering engine/library, needed for aseprite
www.freetype.org 


[Emscripten] -- Converts webgl to opengl and vice versa and c/c++ to 
			node.js and more; needed to compile aseprite; super useful for
      working with multiple graphics libraries
www.emscripten.org


[docker engine] -- powerful for building software within containers
				without needing mess with your root libraries
https://docs.docker.com/engine/

	(Note: needed to compile aseprite, the aseprite docker compile
	script is in your home directory)


[Discord] -- Chat client
www.discord.com


[Steam] -- Digital game licensing marketplace for buying and publishing
www.store.steampowered.com


[cmake] -- simplifies or consolidates build scripts


[LMMS] -- FOSS DAW for making music comes with [Zynthian]
https://lmms.io/


[Zynthian] -- FOSS Synthesizer, powerful, simple, use to make
			instruments or sound fx
https://zynthian.org/


[Audacity] -- Sound engineering software
https://www.audacityteam.org/


[LXDE] - Lightweight Desktop Environment made with gtk3
http://www.lxde.org/


[PIP] - Python apt/dpkg kind of thing for fetching python modules
https://pypi.org/project/pip/
	
	(Note: If you don't intend to use python you can remove this
	and pygame, pyglet3d, and pyopengl. Which maybe free up around
	800mb, you can purge these on the install disc too, to skip
	installing them altogether. Do not remove python3 itself)
	
	
[GTK 4] - quickly and effeciently develop widgets and windows
	
	(Note: Openbox kind of meh and I want to make my own wm 
   	one day. You should remove the gtk4 developer packages if 
   	you don't explicitly want to work with gtk4.)
	

[EasyTether] - Just a personal thing

[OpenSSL] - needed to install easytether

[LogiOps] - Logitech driver, manipulate logitech mmo mice like mine
https://github.com/PixlOne/logiops

[IMPORTANT]
I use nvidi-550 from the ubuntu repository. If you run into problems with
this simply select advanced options->recovery mode->enable networking
then enter Root Shell option and google on your phone your GPU and google
nvidia linux drivers, follow the prompts putting in your gpu, nividia
will give you a list of drivers to install

in the root shell you may also be able to type 


========================================================================

I do not use java really for anything but if you are interested in 
a framework available for java then look into libgdx

I've also included a script/plugin that will add godot-script to geany's
syntax/lexical/semantic highlight and suggestions. 

I've also included the docker script 

I highly recommend running the following if you want a pure lxde
experience. Ignore if you don't mind gnome elements or want to use
gdm

	apt purge gdm3 gnome-shell
	
========================================================================

signed
JenStudios, 
Jennifer :)

jennstudiosgames@gmail.com
r/JenStudios or r/JenStudiosGames





