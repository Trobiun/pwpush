# pwpush
Command line Python password pusher via pwpush.com

If no password argument is given, a 20 character password comprised of letters, digits, and punctuation is generated.

### Usage:

```
usage: pwpush [-h] [-u URL] [-U USER] [-T TOKEN] [-n NOTE] [-p PASSWORD] [-P PASSPHRASE] [-r] [-d DAYS] [-v VIEWS] [-D]

Accept a password from stdin.

options:
  -h, --help            show this help message and exit
  -u URL, --url URL     Optional: Specify the URL of a local pwpush instance. ex: pwpush -u https://foobar.com
  -p PASSWORD, --password PASSWORD
                        Optional: User defined password.
  -P PASSPHRASE, --passphrase PASSPHRASE
                        Optional: Specify passphrase to give to view the created push.
  -r, --retrieval-step  Optional: Flag to avoid chat systems and URL scanners from eating up views.

User authentication:
  -U USER, --user USER  Optional: Specify the user email to login to pwpush instance.
  -T TOKEN, --token TOKEN
                        Optional: Specify the user token to login to pwpush instance.
  -n NOTE, --note NOTE  Optional: If authenticated, the URL encoded note for this push. Visible only to the push creator.

Expiration of pushes:
  -d DAYS, --days DAYS  Optional: Specify the amount of days after which the password should expire. Defaults to 2.
  -v VIEWS, --views VIEWS
                        Optional: Specify the amount of views after which the password should expire. Defaults to 10.
  -D, --deletable       Optional: Flag to allow users to delete password once retrieved.
```

ex.
```
> ./pwpush
Pass is: GKtPq:@%Q'r2Jakf7RQ0
URL: https://pwpush.com/p/tkfrluql1hi0f6qt

> ./pwpush -p foobar -u http://localhost:5100 -v 5
Pass is: foobar
URL: http://localhost:5100/p/630thim25imnm2x1
```
