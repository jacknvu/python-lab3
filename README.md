# python-lab3

Write a script to resize an existing file

**Part1**

1. create a 1MB file (ex: testfile1) using Linux command **truncate** in a subdirectory called lab3
- ex: truncate -s 1M testfile1
2. run: man truncate (to read manual pages)
3. write a Python script to resize the file
4. input the directory name, file name, and new file size
5. list the existing file using "ls -l" command
6. resize file (ex: testfile1 in lab3 subdirectory) to 2MB (using truncate command)
  - Reference:  https://www.youtube.com/watch?v=2Fp1N6dof0Y
  - ex: p1 = subprocess.run('ls -l', shell=True, capture_output=True, text=True)
7. optional: script to validate input arguments, check for null (or zero length) input
8. Sample execution:
<pre>
  $ ./resize3.py 
  enter sub dir:lab3
  enter existing filename:testfile1
  ls -l lab3/testfile1
  -rw-r--r-- 1 pi pi 1048576 Jun  7 21:34 lab3/testfile1
</pre>


**Log in instructions:**

1. log in to host 192.168.1.42 as use pi, run from Mac window:  ssh -l pi 192.168.1.42
2. enter password
3. make your own work subdirectory, ex:  
<pre>
    mkdir jvu.d
    cd jvu.d
    mkdir lab3
</pre>
4. and put the python script in this lab3 subdirectory

**Part2**

1. use **argparse** module to input arguments into the Python script from command line
2. Ex:  ./resize.py -d lab3 -s 2MB testfile1
