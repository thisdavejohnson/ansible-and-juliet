Ansible and Juliet
==================

This is an Ansible playbook, intended to cast a hapless college Mac lab into an unexpected scheduled Shakespearean performance.

Setup
=====

Start with an Ansible install on an OS X control machine, and check out this project:

    cd ansible-and-juliet/

In the hosts file, change the host addresses to computers you wish to enlist:

    vim hosts

    [cast]
    sampson       ansible_ssh_host=127.0.0.1 voice=alex
    gregory       ansible_ssh_host=127.0.0.1 voice=ralph
    abraham       ansible_ssh_host=127.0.0.1 voice=bruce
    tybalt        ansible_ssh_host=127.0.0.1 voice=fred
    benvolio      ansible_ssh_host=127.0.0.1 voice=ralph
    first_citizen ansible_ssh_host=127.0.0.1 voice='pipe organ'
    capulet       ansible_ssh_host=127.0.0.1 voice='cellos'
    lady_capulet  ansible_ssh_host=127.0.0.1 voice=vicki
    montague      ansible_ssh_host=127.0.0.1 voice=zarvox
    lady_montague ansible_ssh_host=127.0.0.1 voice=victoria
    prince        ansible_ssh_host=127.0.0.1 voice=trinoids

Now, when ready, start the performance.  

    ansible-playbook romeo_and_juliet.yml -i hosts -c ssh
 
Your computer lab will spring to life, performing Shakespeare, in computerized voices from Cuppertino.

Bonus points for using workstations people are actually using at the time.

You can test it locally by using "-c local" instead of "-c ssh".

License
=======

As the bard is public domain, so be thus herein, forsooth, like.

Author
======

Michael DeHaan

Exeunt Stage Right
==================

CURTAIN



