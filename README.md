1. **Update your system:**

sudo apt update
sudo apt upgrade

markdown


2. **Install the required packages:**

sudo apt install build-essential dkms

markdown


3. **Remove any previously installed NVIDIA drivers:**

sudo apt remove --purge '^nvidia.*'

markdown


4. **Install the recommended driver for your GPU:**

First, add the graphics-drivers PPA:

sudo add-apt-repository ppa:graphics-drivers/ppa
sudo apt update

rust


Then, install the recommended driver for your GPU:

sudo ubuntu-drivers autoinstall

sql


Alternatively, you can install a specific driver version using:

sudo apt install nvidia-driver-XXX

markdown


Replace `XXX` with the version number you want to install. For the Quadro K5200, version 470 should work well. You can always check the NVIDIA website for the latest compatible driver version.

5. **Reboot your system:**

sudo reboot

markdown


6. **After the system restarts, verify that the driver is installed correctly:**

nvidia-smi

rust


You should see information about your GPU, including the driver version and the GPU's utilization.

If you encounter any issues during the installation process, consult the official NVIDIA documentation or the Ubuntu community forums for additional guidance.

You can copy and paste this text into a Markdown-supported text editor or note-taking app to maintain the formatting.
