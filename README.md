# condor_ql
A Uni-Bonn BAF2-Cluster HTCondor `condor_q` and `condor_history` parser for Python3

Takes the `condor_q` or `condor_history` output (with a specific query) in JSON form and parses it to a nicer and cleaner output.
Options are explained by `condor_ql --help`

Example output of `condor_ql`:
![condor_ql_output](https://github.com/marvinlenk/condor_ql/assets/25794829/9dac37ae-32fe-437f-aa11-87bc9d35953c)

Example output of `condor_ql -hi`:
![condor_ql_hi_output](https://github.com/marvinlenk/condor_ql/assets/25794829/c47480f5-2762-454d-b6a3-d82ec5751397)

How to get it working on your system:
1. Copy the `condor_ql` file into a folder of choice (e.g. `~/.local/bin`) OR clone the repo and create a [symlink](https://stackoverflow.com/a/1951752) to `condor_ql` in the desired folder.

2. Make shure the path to `condor_ql` (or the symlink) is in your `$PATH` variable - if not do the following:
  Change your terminal profile to include the path, e.g. add 
  `export PATH=~/.local/bin:$PATH`
  to your
  `~/.bash_profile`
  file (create one if it doesn't exist)
  
3. (**OPTIONAL** / might not be necessary on your system) Change the path after `#!` in the `condor_ql` file to your Python3.X path. If you are not sure where your Python sits, use
  `which python3`. Please note that Python2 is not supported and likely will not work in this case.

4. Make it executable via executing `chmod +x condor_ql` in the folder where the file `condor_ql` (or the symlink) resides.

5. You might want to restart the terminal session for bash to recognize the new command.

Tada! Now it should work.
Please note, that the command can be slow, just as `condor_q` and especially `condor_history` is.

P.S. This script is not officially supported by the Uni Bonn IT team. You are free to use it, but please don't contact them for support. 
