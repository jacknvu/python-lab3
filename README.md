# python-lab3

Write a script to resize an existing file

**Part1**

1. create a 1MB file (ex: testfile1) using Linux command **truncate** in a subdirectory called lab3
2. run: man truncate (to read manual pages)
3. write a Python script to resize the file
4. input the directory name, file name, and new file size
5. list the existing file using "ls -l" command
6. resize file (ex: testfile1 in lab3 subdirectory) to 2MB (using truncate command)
  - Reference:  https://www.youtube.com/watch?v=2Fp1N6dof0Y
  - ex: subprocess.run('ls -l', shell=true, capture_output=true, text=true)
8. script to validate input arguments, check for null (or zero length) input

**Log in instructions:**

1. log in to host 192.168.1.42 as pi:  ssh -l pi 192.168.1.42
2. enter password
3. make your own subdirectory, ex:  mkdir jvu.d; cd jvu.d and put the python script in this subdirectory

**Part2**

1. use **argparse** module to input arguments into the Python script from command line
2. Ex:  ./resize.py -d lab3 -s 2MB testfile1
