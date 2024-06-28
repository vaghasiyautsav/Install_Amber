# Install_Amber
How to Install Amber24 (&amp;AmberTools24) into Ubuntu.

## Installation Steps
1. Extract Amber Archives
First, extract the Amber archives in /home. Replace AmberTools16 and Amber16 with the appropriate version numbers for Amber24.
```
tar xvfj AmberTools24.tar.bz2
tar xvfj Amber24.tar.bz2
```
## 2. Set AMBERHOME Environment Variable
Determine your current directory and set the AMBERHOME environment variable:
pwd
```
export AMBERHOME=/home/yourusername/amber24
```
- Replace /home/yourusername with your actual home directory path.
## 3. Install Dependencies
Install necessary dependencies:
```
sudo apt-get install csh flex gfortran g++ xorg-dev zlib1g-dev libbz2-dev patch python-tk
```
## 4. Source Amber Environment
Source the Amber environment file:
```
source /home/yourusername/amber24/amber.sh
```
- Replace /home/yourusername with your actual home directory path.
## 5. Compile and Test Amber
Compile Amber and run tests:
```
make install
make test
```
- This process may take some time.
## 6. Set Up Amber Environment Permanently
Add the Amber environment to your .bashrc file:
```
sudo nano ~/.bashrc
```
Add the following line at the end of the file:
```
source /home/yourusername/amber24/amber.sh"
```
Save (Ctrl+O, Enter) and exit(Ctrl+X) the editor. 
Then, source your updated .bashrc:
```
source ~/.bashrc
```

## Verification
To verify the installation, open a new terminal and type:
```
tleap
```
This should display the version information like below
```
-I: Adding /home/username/amber24/dat/leap/prep to search path.
-I: Adding /home/username/amber24/dat/leap/lib to search path.
-I: Adding /home/username/amber24/dat/leap/parm to search path.
-I: Adding /home/username/amber24/dat/leap/cmd to search path.

Welcome to LEaP!
(no leaprc in search path)
>
```
- Exit By putting "quit".

## Troubleshooting
For detailed troubleshooting, refer to the Amber Manual: https://ambermd.org/doc12/Amber20.pdf
Additional Resources
Official Amber Website: https://ambermd.org/index.php
Amber24 Documentation: https://ambermd.org/doc12/Amber20.pdf

## License
Please ensure you comply with Amber's licensing terms. Amber is not free software and requires a license for use.
