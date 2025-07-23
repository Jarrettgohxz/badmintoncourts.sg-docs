# Badminton Courts SG

![alt text](go_badminton.png)

Ever wanted to find a badminton court in Singapore, but ended up stuck manually clicking through every single venue just to check one date? Well, as an active Badminton player, I understand your struggle as I’ve been through that pain way too many times. But not to worry, I got you 😉.

Introducing a simple automation software written in the [Go](https://go.dev/) <img src="golang.png" width="30" height="30"/> programming language. It provides a compiled listing of Badminton courts around Singapore.

Check out the live webpage at https://badmintoncourts.sg. Currently, it only supports the following sources: **ActiveSG** and **OnePA**, with plans to extend to private courts soon :) _OH YEAH_, and guess what? It even comes with a map display for an easy and interactive location-based view!

> # **IMPORTANT NOTICE**

**`1.`** The main purpose of this program is to simplify the process of finding Badminton courts. There are **_NO intentions of causing harm or disruption_** to the external sources involved.

**`2.`** It **DOES NOT** (and never will) deal with booking of courts in any way

**`3.`** It is built with safety in mind, and extra precaution is taken to ensure that requests are limited, to reduce the stress on servers

**`4.`** There is only a **_SINGLE_** process at any point in time that is communicating with the external servers, while other concurrent processes will read data from a cached database file instead

- this single process limits the requests to a _maximum_ pool of _6-8 goroutines_, ensuring **_controlled_** and **_predictable_** traffic towards upstream external sources
- this prevents any form of disruption to the services

**`5.`** The program will only send a new batch of requests to the external servers after a period of time have passed (**10 minutes**), and would otherwise retrieve data from a cached database file instead

- in other words, the data is only refreshed at every fixed interval, preventing any form of spam request to the upstream source servers

## Technical Overview
```
        ASCII generated with https://convertcase.net/ascii-art-generator/
          -==-                          ..
        .=-:--*.                        ::   _::
       .--==--:=.                       :::-..  ::
      .=-----=-=-.                      ::-::.:::
      :=:=-=--=--.                     .--:--:   ::
     .+.=-=-=--+-.                    .:=-=---.:.:  ::
     ----=-=-=---.                     -=+=::.:--:--:
     -==--=-=---:.          .--.       ####:.:-- Gopher playing badminton! ~ written in Go (Jarrettgohxz)
     -=-==-+-=.-.           ---:      :--.###    
     .==--=:=:-:.. ..:======++=:.     .-._~~|
      -=---=-=::--.:--:......:+=-:.
      .*+=++=:::::=-.===.    ---:-:
       +-+... +:+-.:*..:*:  -:  ..=.
      .#-.    :---.-. ...-:.+  -#=-:
      -=       -=.-:  .#=.-:+. -#=:-
     .+.       :: =.  :#.--+=....-=  .-:+:.
    .:-        =. =:  .::.+#==+..:-+. .+==++.
    .*:        =  .-:. .:-====-=--.-: .=..=+.
    +*:        =   .-===-:=.-==-:. .-.-. :-.
   +-++.       =     ... .-*:=-.    ==: .-.
  .+*+:=       =           -:+=.    +.  ::
  :**+.--.     =           .-:..    +. :-.
  =#+-..:==-----            .       =.--.
   :..=:. .:::-                     =+:
      .--:..                        =:
        .:--===                     -:
          ...=:                     -:
            .=                      -:
            .-                      =.
            ::                      =
          .:-:                     .=
          :==-                     -:
          .-==                    .=.
           ..+.                  .-.
            .-:                  :-.
          .--: ...             .-=.
         .=:..==-=:          .:=:-.
         .*:.=.  .=+=:.   ..-++: ::
          =+-.......:-=====-:..=.-=-.
        ..:---=================+:::+=-:.

```

## Feedback

- I would greatly appreciate any feedback or comments regarding the entire project.
## Pending Features

**`1.`** Additional sources to add

- Singapore Badminton Hall
  https://singaporebadmintonhall.com/book-now/

- Singapore Badminton
  https://booking.singaporebadminton.org.sg/

- SmashArena
  https://booking.smasharena.sg/

- WYSE Active
  https://wyseactivehub.rezerv.co/appointment-booking?apptId=96296a8a-5b90-4823-b9a1-e6d1fa1c6589&locationId=bdfe0e1f-b01a-48de-977c-2afbd2b15252

- Optimum Badminton Academy
  https://optimumbadmintonacademy.com/court-booking

- TruSmash
  https://book.afa-sports.com/scheduler

- Any other source you would like to add?

**_Have any new ideas?_**

> Feel free to email me at *jarrettgoh.xz@gmail.com* regarding any features you would like to add on.

**_Like this project?_**

Do check out my personal portfolio website at https://gohxiangzheng.com, for a list of all my projects, ranging from web/mobile development, automations (shell scripting), computer networking and cybersecurity!
