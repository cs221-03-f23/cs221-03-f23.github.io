---
layout: assignment
due: 2023-08-29 23:59:59 -0800
permalink: assignments/lab01.html
title: Lab01 - Environment Setup
github_url: https://classroom.github.com/a/xJREGGYk
---

## Background

1. You will develop course assignments using the CS department `vlab` hosts
1. In order to connect to `vlab` hosts, you will `ssh` through `stargate`, the CS department jump server.
1. To use `ssh`, you will set up an `ssh` keypair to connect securely
1. You will also use `ssh` to securely push your solutions to `github.com` using `git`

## Step 1: Configure `ssh` to use with `github.com`

1. The first step is to set up your `ssh` keypair on your laptop, and paste your public key onto `github.com`
1. Follow [these instructions](/docs/ssh-local-setup.html) to do that

## Step 2: Configure `ssh` to use with `stargate`

1. After you have `ssh` working between your laptop and `github.com` you can follow [these instructions](/docs/ssh-stargate-setup.html) to connect with the CS Labs network environment and use `ssh` from `vlab` hosts to `github.com`


## Step 3: Finally, some code
1. Accept the GitHub assignment [here](https://classroom.github.com/a/xJREGGYk) 
1. Clone the assignment repository ("repo") into your home directory
    ```sh
    YOUR_USF_USERNAME@vlab01:~ $ git clone git@github.com:/cs221-s23/lab01-YOUR_GITHUB_USERNAME
    YOUR_USF_USERNAME@vlab01:~ cd lab01-YOUR_GITHUB_USERNAME
    ```
1. Compile the program
    ```sh
    YOUR_USF_USERNAME@vlab01:lab01-YOUR_GITHUB_USERNAME $ gcc -o hello hello.c
    ```
1. Run the program
    ```sh
    YOUR_USF_USERNAME@vlab01:lab01-YOUR_GITHUB_USERNAME $ ./hello
    hello world
    ```
1. Edit `hello.c` and change `"hello world\n"` to `"hello cs221\n"` in lower case exactly as shown
1. Save the file and recompile it
1. Commit your changes to the local repo on the lab machine
    ```sh
    YOUR_USF_USERNAME@vlab01:lab01-yourgithubid $ git commit -m"change world to cs221" hello.c
    ```
1. Push your changes from the local repo to the remote repo on `github.com``
    ```sh
    YOUR_USF_USERNAME@vlab01:lab01-yourgithubid $ git push
    ```
1. `^D` to log out of the lab host, and again to log out of `stargate`

<script>
    function toggle_display(id_name) {
        var e = document.getElementById(id_name);
        if (e.style.display === "none") {
            e.style.display = "block";
        } else {
            e.style.display = "none";
        }
    }
</script>
