<div align="center">
<img src="./assets/logo.png" alt="Logo" style="width: 300px" />
<h1>Tilence</h1>
</div>

Tilence is a GNOME Shell extension turning off notifications while sharing screen during a Kontur Talk call.

(Fork of - (https://github.com/apankowski/zilence/)


It does so by:

* tracking presence of Talk's screen sharing panel (seen at the top-center of the screen),
* switching "Do Not Disturb" setting accordingly.

## Reporting issues

Please report issues [on GitHub](https://github.com/RedFraction/tilence/issues), providing:

* OS version (can be found in _Settings_ → _About_ → _OS Name_ and _OS Type_),
* GNOME version (can be found in _Settings_ → _About_ → _GNOME Version_),
* Zoom client version (can be found in _Zoom menu_ → _Help_ → _About Zoom_)

and attaching extension logs since last boot:

```bash
journalctl -b | grep -i tilence > tilence.log
```

(the command above will save logs in `zilence.log` file).

## Building

To build the extension from source you'll need `git` and `jq`. You can install these using the following command:

```shell
sudo apt-get install git jq
```

Then run the following command in project's root directory:

```shell
./build.sh
```

In the same directory you'll find the zip file with packaged extension.
