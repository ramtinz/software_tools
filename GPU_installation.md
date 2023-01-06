The availability of a GPU on a system depends on the hardware configuration of the system. If a GPU is not available on a system, it cannot be installed or added later.

However, you can use the lspci command to check if a GPU is available on a system. For example, you can use the following command to list the PCI devices on the system:

>lspci | grep -i "vga"

This will list any devices that have the "VGA" string in their PCI ID, which typically indicates a GPU. If no devices are listed, it means that a GPU is not available on the system.

Note that this will only work if the system has a PCI-based GPU. If the system has an integrated GPU (such as an Intel or AMD GPU), it will not be listed by lspci and cannot be detected in this way.

To check GPU jobs on a Linux system, you can use the nvidia-smi command, which is a tool provided by NVIDIA for monitoring and managing NVIDIA GPUs.

To view a list of the currently running GPU jobs, you can use the following command:

>nvidia-smi

This will display the GPU utilization in percent, updated every second. You can press Ctrl+C to stop the output.

Note that the nvidia-smi command is only available on systems that have an NVIDIA GPU. If the system does not have an NVIDIA GPU, this command will not be available.
