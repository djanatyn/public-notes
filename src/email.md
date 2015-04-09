= email on zubkoland

zubkoland uses the http://www.postfix.org/[postfix] mail server to both receive and send mail, and the http://www.courier-mta.org/maildrop/[maildrop] delivery agent for delivering mail. new users have a directory, $HOME/Mail/, in which mail addressed to them is sent. in practice, this means that you'll configure your mail user agent (or MUA) to use messages there.

zubkoland has http://en.wikipedia.org/wiki/Mutt_%28email_client%29[mutt], a popular command line mail client installed. to get started with mail quickly, put this as the contents of $HOME/.muttrc:

----
set folder="~/Mail"
set mask="!^\\.[^.]"
set mbox="~/Mail"
set record="+.Sent"
set postponed="+.Drafts"
set spoolfile="~/Mail"
set from="Your Name <username@zubkoland.org>"
----

you should then be able to run mutt to read, write, and send messages.
