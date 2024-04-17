# condor_ql
A Uni-Bonn BAF2-Cluster HTCondor `condor_q` and `condor_history` parser for Python3

Takes the `condor_q` or `condor_history` output (with a specific query) in JSON form and parses it to a nicer and cleaner output.
Options are explained by `condor_ql --help`

How to get it working on your system:
1. Copy the `condor_ql` file into a folder of choice (e.g. `~/.local/bin`) OR clone the repo and create a symlink to `condor_ql` in the desired folder.

2. Make shure the path to `condor_ql` (or the symlink) is in your `$PATH` variable - if not do the following:
  Change your terminal profile to include the path, e.g. add 
  `export PATH=~/.local/bin:$PATH`
  to your
  `~/.bash_profile`
  file (create one if it doesn't exist)
  
3. (OPTIONAL / might not be necessary on your system) Change the path after #! to your Python3.X in the `condor_ql` file. If you are not sure where your Python sits, use:
  `which python3`
  You may have to plug in the command you use to open Python, but make sure it is version 3.0 or newer !!!

4. Make it executable via executing
  `chmod +x condor_ql`
  in the folder where `condor_ql` (or the symlink) resides.

5. You might want to restart the terminal session for bash to recognize the new command.

Tada! Now it should work.
Please note, that the command can be slow, just as `condor_q` and especially `condor_history` is.
