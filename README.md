# Sharif Judge

[Sharif Judge](http://sharifjudge.ir) is a free and open source online judge for C, C++, Java and
Python programming assignments. It can also be used for programming contests, but it has features
specially for programming assignments.

Installation doesn't need root privileges.
The web interface is written in PHP (CodeIgniter framework) and the main backend is written in BASH.

Python in Sharif Judge is not sandboxed yet. Just a low level of security is provided for python.
If you want to use Sharif Judge for python, USE IT AT YOUR OWN RISK or provide sandboxing yourself.

The full documentation is at [http://docs.sharifjudge.ir](http://docs.sharifjudge.ir)

Download the latest release from [http://sharifjudge.ir/download](http://sharifjudge.ir/download)

## Features
  * Multiple user roles (admin, head instructor, instructor, student)
  * Sandboxing _(not yet for python)_
  * Cheat detection (similar codes detection) using [Moss](http://theory.stanford.edu/~aiken/moss/)
  * Custom rule for grading late submissions
  * Submission queue
  * Download results in excel file
  * Download submitted codes in zip file
  * _"Input/Output Comparison"_ and _"Tester Script"_ methods for checking output correctness
  * Add multiple users
  * Rejudge
  * Scoreboard
  * Notifications
  * ...

## Requirements

For running Sharif Judge, a Linux server with following requirements is needed:

  * Webserver running PHP version 5.3 or later with `mysqli` extension
  * PHP CLI (PHP command line interface, i.e. `php` shell command)
  * MySql database
  * PHP must have permission to run shell commands using [`shell_exec()`](http://www.php.net/manual/en/function.shell-exec.php) php function (specially `shell_exec("php");`)
  * Tools for compiling and running submitted codes (`gcc`, `g++`, `javac`, `java`, `python` and `python3` commands)
  * It is better to have `perl` installed for more precise time and memory limit and imposing size limit on output of submitted code.

## Installation

  1. Download the latest release from [download page](http://sharifjudge.ir/download) and unpack downloaded file in your public html directory.
  2. Create a MySql database for Sharif Judge.
  3. Set database connection settings in files `application/config/database.php` and `tester/queue_process.php`. Make sure that you have provided correct information in both files.
  4. Open Sharif Judge main page in a web browser and follow the installation process.
  5. Log in with your admin account.
  6. **[IMPORTANT]** Move folders `tester` and `assignments` somewhere outside your public directory. Then save their full path in `Settings` page. **These two folders must be writable by PHP.** Submitted files will be stored in `assignments` folder. So it should be somewhere not publicly accessible.
  7. **[IMPORTANT]** [Secure Sharif Judge](http://docs.sharifjudge.ir/security)

## After Installation

  * Read the [documentation](http://docs.sharifjudge.ir/installation#after_installation)
