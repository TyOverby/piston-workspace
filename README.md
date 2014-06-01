piston-workspace
================

Git submodules of Piston projects

## How to build Piston

```
git clone --recursive https://github.com/PistonDevelopers/piston-workspace.git
cd piston-workspace
chmod +x build.sh
./build.sh
```

## Piston symlink files

A symlink file allows you to rebuild Piston without needing to copy the '.rlib' files each time.  
When you have built Piston, the symlinks should be located in the folder 'piston-symlinks/'.  
These can be copied and put in the 'target/cpu-vendor-os/lib/' folder in your project.  

To tell the Rust compiler to look for the Piston rlib file, add `extern crate piston;` to your source.  

## How to setup a new project

1. copy 'Makefile' from https://github.com/bvssvni/rust-empty to a new empty folder
2. open up the Terminal window and navigate to the project folder
3. type make run to create "hello world!" example
4. copy symlinks from 'piston-symlinks/' to the projects 'target/cpu-vendor-os/lib/' folder
5. add `extern crate piston;`, `extern crate graphics;` etc. to your source at top level

## How to upgrade to Rust master

This information is for PistonDevelopers:

```
chmod +x update.sh
./update.sh
```

If you find Piston-Workspace out of date, run this script and do a build.  
Check that there are no errors and send a pull request.  
