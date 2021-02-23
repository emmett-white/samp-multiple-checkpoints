# multiple-checkpoints-samp

[![sampctl](https://img.shields.io/badge/sampctl-multiple--checkpoints--samp-2f2f2f.svg?style=for-the-badge)](https://github.com/emmett-white/multiple-checkpoints-samp)

This include lets you create more than one checkpoint at the same time!(Requires Incognito's Streamer)

<a href="https://ibb.co/zX4JTJc"><img src="https://i.ibb.co/hBmfJf5/photo-2021-02-23-00-34-07.jpg" alt="photo-2021-02-23-00-34-07" border="0"></a>

<a href="https://imgbb.com/"><img src="https://i.ibb.co/3mb9gFp/photo-2021-02-23-00-34-08.jpg" alt="photo-2021-02-23-00-34-08" border="0"></a>

## Installation

Simply install to your project:

```bash
sampctl package install emmett-white/multiple-checkpoints-samp
```

Include in your code and begin using the library:

```pawn
#include <multiple-checkpoints-samp>
```

# Functions:

#### ShowCP(playerid, Float:x, Float:y, Float:z)
>* **Parameters:**

>       playerid - The id of the player to create checkpoint for
>       Float:x, Float:y, Float:z - The position of the checkpoint
>* **Returns:**

>       INVALID_CP_ID(-1) if failed to create the checkpoint
>       The id of the checkpoint if successful
>* **Remarks:**

>       It will print an error message if it fails to create the checkpoint(player is not connected or there's no available free map icon for that player)

#### DestroyCP(playerid, cpid)
>* **Parameters:**

>       playerid - The id of the player to destroy the checkpoint for
>       cpid - The id of the checkpoint to destroy(Returned by ShowCP)
>* **Returns:**

>       0 if didn't execute successfully(Invalid checkpoint id)
>       1 if function executed successfully
>* **Remarks:**

>       It will print an error message if it fails to destroy the checkpoint(cpid is invalid or player is not connected)

# Callbacks:

#### OnPlayerEnterCP(playerid, cpid)
>* **Parameters:**

>       playerid - The id of the player who triggered the checkpoint
>       cpid - The id of the checkpoint player has triggered

#### OnPlayerLeaveCP(playerid, cpid)
>* **Parameters:**

>       playerid - The id of the player who triggered the checkpoint
>       cpid - The id of the checkpoint player has triggered


To test, simply run the package:

```bash
sampctl package run
```