By default, the images start in the REPL, or you can run `sh` to use `cpanm` etc.

The REPL can be run explicitly with `re.pl`.

```
$ docker run --rm -it razerm/perl-repl sh
/ # cpanm DBI
--> Working on DBI
Fetching http://www.cpan.org/authors/id/T/TI/TIMB/DBI-1.636.tar.gz ... OK
Configuring DBI-1.636 ... OK
Building and testing DBI-1.636 ... OK
Successfully installed DBI-1.636
1 distribution installed
/ # re.pl
$ use DBI;
```

The `slim` tag doesn't have build dependencies.

```
$ docker run --rm -it razerm/perl-repl:slim
$ my @names = ("Foo", "Bar", "Baz");
$VAR1 = 'Foo';
$VAR2 = 'Bar';
$VAR3 = 'Baz';
```