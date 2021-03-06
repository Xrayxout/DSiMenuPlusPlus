# DSiMenu++
DSiMenu++ is an open-source DSi Menu upgrade/replacement, and frontend for nds-bootstrap for DSi, and flashcards.

# Building

Building this app by yourself require DEVKITARM with DEVKITPRO. You will also need [Easy GL2D](https://www.odrive.com/s/eb3e676a-be1b-4a18-bc7d-67f25c80eb42-5917ab0b). Merge the contents `LibGL2D_DS.zip:/distributable/libnds/* (lib and include)` at `devkitPro/libnds/`. Also, download [this](https://www.odrive.com/s/895059a5-673c-4b3c-b3dd-8dbf0cbd8c6f-5af9d7f4) file, and place it at `devkitPro/libnds/lib`, overwriting the existing one.
Make sure that grit and mmutil are installed.

# Building with Docker

DSiMenu++ comes included with a Docker image for easy building without having to manually set up the required version of devkitARM and Easy GL2D. 

## Building with Docker for Windows users.

You can compile DSiMenu++ with Docker using the provided PowerShell (`.ps1`) scripts. First, install docker at http://docker.com, and [configured Shared Drives](https://blogs.msdn.microsoft.com/stevelasker/2016/06/14/configuring-docker-for-windows-volumes/) for the drive where DSiMenu++ is cloned. 

Then run `compile_docker.ps1` in a PowerShell window. The script accepts `make` arguments as well, for example `.\compile_docker.ps1 clean`. Note that Docker compilation is not compatible with native Windows compilation. You should run `.\compile_docker.ps1 clean` to clean the artifacts before attempting to build with Docker.

To build all artifacts, run `.\compile_docker.ps1 package`.

# Credits

- ahezard: [nds-bootstrap](https://github.com/ahezard/nds-bootstrap)
- Apache Thunder: DS menu top screen image.
- Joom: Original TWLoader logo.
- me: For implementing the auto-reset power button function used in NTR-mode, and LED functions, to nds-bootstrap.
- shutterbug2000: For the muted sound/touchscreen fix for nds-bootstrap.
- spinal_cord: DSi4DS assets.
