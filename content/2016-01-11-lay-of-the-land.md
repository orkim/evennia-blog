Title: Lay of the Land
Date: January 11, 2016
Author: orkim
Category: Evennia
Tags: mud

## Current Status

I've been playing with Evennia again for a few days now and I've decided that
it would be a good time to review what comes stock from an install.

In doing so, I've also come across a few bugs and submitted bug reports like a
good OSS user.  Once that was complete, I set out to fix them myself. But for
the purpose of this review we will assume those bugs are already fixed.

## What do we have available?

I started off with a "normal user" and not using the super user account. This
account is more limited, and thus has a smaller help file. I logged in as that
user, and issued a "help" command.

    ------------------------------------------------------------------------------
       Command help entries
    ------------------------------------------------------------------------------
      Channel Names:
    public
      Comms:
    @cboot, @ccreate, @cdesc, @cdestroy, @cemit, @channels, @clock, @cwho, addcom,
    allcom, delcom, page
      General:
    @charcreate, @color, @ic, @ooc, @option, @password, @quell, @quit, @sessions,
    access, desc, drop, get, give, help, inventory, look, nick, pose, say, who
      System:
    @about, @time

So, going over the output a bit we can see things are broken into nice
categories for us to work though. Let's go through them in order.

## Channel Names

This lists the names of the channels that I am currently subscribed (meaning I
will get output from those channels if someone talks on them). These are also
the command(s) to speak on that channel. Since I'm only subscribed to a single
public channel by default, there is only one entry: `public`.

Issuing a `public Hellllllo out there.` will post the text "Hellllllo out
there." to the channel.

## Comms

These commands deal with channels mostly. There are a number of commands to
administrate a channel (if you have permission). These are pretty self
explanatory, so we'll just sum them up quickly.

  * `@cboot` - Kick a player from a channel.
  * `@ccreate` - Create a new channel.
  * `@cdesc` - Set a channels description.
  * `@cdestroy` - Destroy a channel.
  * `@cemit` - Sends an admin message to a channel.
  * `@channels` - Lists all channels.
  * `@clock` - Sets the channel locks on a channel.
  * `@cwho` - Lists the users subscribed to a channel.

And we also have commands for managing your own channel subscriptions.

  * `addom` - Subscribe to a new channel, or add an alias for a channel.
  * `allcom` - Operations on all channels (on, off, who, destroy).
  * `delcom` - Unsubscribe to a channel, or remove an alias for a channel.

And finally we have a command to speak directly with another player. This is
`page` (it has an alias of `tell` as well). This is the command to send a
private message to another player on the MUD.

## General

  * `@charcreate` -
  * `@color` -
  * `@ic` -
  * `@occ` -
  * `@option` -
  * `@password` -
  * `@quell` -
  * `@quit` -
  * `@sessions` -
  * `access` -
  * `desc` -
  * `drop` -
  * `get` -
  * `give` -
  * `help` -
  * `inventory` -
  * `look` -
  * `nick` -
  * `pose` -
  * `say` -
  * `who` -

## System

A few commands related to the MUD itself.

  * `about` - Shows some information about the MUD and versions of software.
  * `time` - Shows the uptime, total runtime, in-game time, and server time.
