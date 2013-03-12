---
layout: post
category: note
title: Echo like a hacker
date: 2013-03-12
summary: Use echo in hackers' way
---

echo command have always called as a simple way to print STRING
to standard output.

As a linux user, you will frequantly saw this...

{% highlight bash %}
$ echo Hello World > hello.txt
$ cat hello.txt
Hello World
{% endhighlight %}

From above, you can see we used the echo to perform simple job in a hacker's way

# Use 'echo' to list content

We usually used 'ls' command to list the content in a directory. But...
we can simple used 'echo' to list down what we want. Talk is cheap, let's see this...

{% highlight bash %}
$ ls
brown.txt    blue.txt   black.txt   red.txt
yellow.txt   Hello.c
$ echo b*
brown.txt blue.txt black.txt
{% endhighlight %}

Awesome! It just list all the content name started with b.

You can also list prefix with...

{% highlight bash %}
$ ls
a.c   b.c   c.c   d.out
$ echo *.c
a.c b.c c.c
{% endhighlight %}

# Use 'echo' to display current username

Although using 'pwd' can easily print current username as well, but since we are a hacker, we must think differently :)

{% highlight bash %}
$ whoami
Leo
$ echo $USER
Leo
{% endhighlight %}

# Use 'echo' to display current user directory

Those sysadmin who are playing with multiple user in linux can use 'echo' to display current user's directory.

{% highlight bash %}
$ whoami
Leo
$ echo ~
/home/Leo
{% endhighlight %}

# 'echo' makes calculation too!

Someone will think this is insane, but it really did! By using $ string...

{% highlight bash %}
$ echo $((2+3))
5
{% endhighlight %}

# There is more trick you can't imagine

{% highlight bash %}
$ echo count-{1,2,3}
count-1 count-2 count-3
$ echo write-{a,b,c}
write-a write-b write-c
$ echo Number{1..3}
Number1 Number2 Number3
{% endhighlight %}

