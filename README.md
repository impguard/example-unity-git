# example-unity-git

A git repository that is unity ready.

## Getting Started

Since Unity does not let one create a new project in an existing directory,
you'll have to create the Unity project first and initialize Git inside of the
project directory (instead of cloning this repo and creating a Unity project in
it).

First, fork this repository or create a new repository on Github mirroring this
one (this will ultimately be your Unity Git project). Then, create a new Unity
project locally on your computer. Navigate to this directory and run:

```bash
git init
git remote add origin <the Github repo remote url>
git fetch
git co origin/master
```

You'll need to install [git-lfs](https://git-lfs.github.com/) in order to push
media files efficiently into git. On Mac with Homebrew, this is as easy as:

``` bash
brew install git-lfs
git lfs install
```

You'll also need to configure your .gitconfig to use
[Unity's custom smart merge](http://docs.unity3d.com/Manual/SmartMerge.html).

Finally, configure your Unity project to
[save Scene files in YAML](https://docs.unity3d.com/Manual/TextSceneFormat.html).
This corresponds to adjusting the Asset Serialization mode be text based.

Once all of this done, you should be able to start adding your Unity files into
your Github repository like normal!
