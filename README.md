# Owlchart

This utility is built on the back of the work done 
[over here](https://github.com/cornetp/eagle-owl) to link to an OWL CM160 device and
download the recorded power data.

It relies on a path to the associated SQLite database, as described in the
documentation for the above software and generates charts based on this
information.

Usage is as follows:

    owlchart <fromdate> <todate>

where `fromdate` and `todate` are formatted as follows: `YYYY-mm-dd`, e.g.,
`2019-02-05`.

Currently the chart file that's generated is in svg format, is named based on
the given from and to dates, and is placed in the current directory.

In order to get going, make sure that the path to the energy data SQLite
database is available—do this by copying `config.py.templ` to `config.py` (per
the instructions in the `config.py.templ` file) and then edit the latter.
Ensure that the `config.db_path` parameter line is uncommented, and points to
the SQLite database file.
