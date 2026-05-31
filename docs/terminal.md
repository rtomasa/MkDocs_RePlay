# Linux Terminal Access

Some advanced tasks require access to the RePlayOS Linux terminal. The usual way to access it is through SSH from another computer on the same network.

## Find the IP address

Before connecting from your PC to RePlayOS, you need to know its IP address. You can find it from `REPLAY OPTIONS > INFORMATION`.

If you are connected with a network cable, use the value shown as `ETHERNET IP`.

## Connect with SSH

Open a terminal on your computer and run:

```sh
ssh root@<replay-ip>
```

Use the password `replayos` when prompted.

## Stop RePlay for maintenance commands

Some commands require the RePlay frontend to be stopped first:

```sh
systemctl stop replay.service
```

To start RePlay in the foreground and view its output in your SSH terminal:

```sh
cd /opt/replay
./replay
```

To stop the foreground process, press `Ctrl + C`.
