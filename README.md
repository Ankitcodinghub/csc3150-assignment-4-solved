# csc3150-assignment-4-solved
**TO GET THIS SOLUTION VISIT:** [CSC3150 Assignment 4 Solved](https://www.ankitcodinghub.com/product/csc3150-assignment-4-solved-4/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;121156&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;2&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (2 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSC3150 Assignment 4 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (2 votes)    </div>
    </div>
Homework Requirements

Environment

We recommend you to do the next two assignments using 1) the cluster, and 2) computers in TC301 classroom (40 available PCs). Please compile and test your code on the cluster before submission. (The cluster and slurm manual is on CSC4005_Slurm User Guide · GitHub, which will be introduced in tutorials)

Submission

Violation against the format requirements will lead to grade deduction.

Here is the format guide. The project structure is illustrated as below. You can also use tree command to check if your structure is fine. Structure mismatch would cause grade deduction.

Please compress all files in the file structure root folder into a single zip file and name it using your student id as the code showing below and above, for example,

Assignment_4_120010001.zip. The report should be submitted in the format of pdf, together with your source code. Format mismatch would cause grade deduction. Here is the sample step for compress your code.

main@ubuntu:~/Desktop$ zip -q -r Assignment_4_&lt;student_id&gt;.zip Assignment_4_&lt;student_id&gt; main@ubuntu:~/Desktop$ ls

Assignment_4_&lt;student_id&gt; Assignment_4_&lt;student_id&gt;.zip

Task Description

In Assignment 4, you are required to implement a mechanism of file system management via GPU’s memory.

Background:

File systems provide efficient and convenient access to the disk by allowing data to be stored, located, and retrieved easily.

A file system poses two quite different design problems. The first problem is defining how the file system should look to the user. This task involves defining a file with its attributes, the operations allowed on a file, and the directory structure for organizing files.

The second problem is creating algorithms and data structures to map the logical file system on to the physical secondary-storage devices.

The file-organization module knows about files and their logical blocks, as well as physical blocks. By knowing the type of file allocation used and the location of the file, the fileorganization module can translate logical block address to physical block address for the basic file system to transfer.

Each file’s logical blocks are numbered from 0 (or 1) through N. Since the physical blocks containing the data usually do not match the logical numbers, a translation is required to locate each block.

The logical file system manages metadata information.

Metadata includes all of the file-system structure except the actual data (or contents of the files).

The file-organization module also includes the free-space manager, which tracks unallocated blocks and provides these blocks to the file-organization module when requested.

The logical file system manages the directory structure to provide the file-organization module with the information the latter needs, given a symbolic file name. It maintains file structure via file-control blocks.

A file-control block (FCB) (an inode in UNIX file systems) contains information about the file, including ownership, permissions, and location of the file contents.

Because there have no OS in GPU to maintain the mechanism of the logical file system, we can try to implement a simple file system in CUDA GPU with single thread, and limit global memory as volume.

The GPU File System we need to design:

We take the global memory as a volume (logical drive) from a hard disk.

No directory structure stored in volume, only one root directory, no subdirectory in this file system.

A set of file operations should be implemented.

In this project, we use only one of GPU memory, the global memory as a volume. We don’t create the shared memory as physical memory for any data structures stored in, like system-wide open file table in memory.

In this simple file system, we just directly take the information from a volume (in global memory) by single thread.

Specification:

The offset of the opened file associated with the read pointer is 0 (always read the file from head).

List information about files.

Implement gsys() to pass the LS_D / LS_S commands.

Template structure:

The storage size of the file system is already pre-defined as:

#define SUPERBLOCK_SIZE 4096 //32K/8 bits = 4 K

#define FCB_SIZE 32 //32 bytes per FCB

#define FCB_ENTRIES 1024

#define VOLUME_SIZE 1085440 //4096+32768+1048576

#define STORAGE_BLOCK_SIZE 32

#define MAX_FILENAME_SIZE 20

#define MAX_FILE_NUM 1024

#define MAX_FILE_SIZE 1048576

#define FILE_BASE_ADDRESS 36864 //4096+32768

// data input and output

__device__ __managed__ uchar input[MAX_FILE_SIZE];

__device__ __managed__ uchar output[MAX_FILE_SIZE];

// volume (disk storage)

__device__ __managed__ uchar volume[VOLUME_SIZE];

At first, load the binary file, named data.bin to input buffer (via load_binarary_file() ) before kernel launch.

Launch to GPU kernel with single thread.

// Launch mykernle function on GPU with single thread mykernel&lt;&lt;&lt;1, 1&gt;&gt;&gt;(input, output);

In kernel function, initialize the file system we constructed.

// Initilize the file system FileSystem fs;

fs_init(&amp;fs, volume, SUPERBLOCK_SIZE, FCB_SIZE, FCB_ENTRIES,

VOLUME_SIZE,STORAGE_BLOCK_SIZE, MAX_FILENAME_SIZE,

MAX_FILE_NUM, MAX_FILE_SIZE, FILE_BASE_ADDRESS);

__device__ void fs_init(FileSystem *fs, uchar *volume, int SUPERBLOCK_SIZE, int FCB_SIZE, int FCB_ENTRIES, int VOLUME_SIZE, int STORAGE_BLOCK_SIZE, int MAX_FILENAME_SIZE, int MAX_FILE_NUM, int MAX_FILE_SIZE, int

FILE_BASE_ADDRESS)

{

// init variables fs-&gt;volume = volume;

// init constants

fs-&gt;SUPERBLOCK_SIZE = SUPERBLOCK_SIZE; fs-&gt;FCB_SIZE = FCB_SIZE; fs-&gt;FCB_ENTRIES = FCB_ENTRIES; fs-&gt;STORAGE_SIZE = VOLUME_SIZE; fs-&gt;STORAGE_BLOCK_SIZE = STORAGE_BLOCK_SIZE; fs-&gt;MAX_FILENAME_SIZE = MAX_FILENAME_SIZE; fs-&gt;MAX_FILE_NUM = MAX_FILE_NUM; fs-&gt;MAX_FILE_SIZE = MAX_FILE_SIZE; fs-&gt;FILE_BASE_ADDRESS = FILE_BASE_ADDRESS;

}

In kernel function, invoke user_program to simulate file operations for testing. We will replace the user program with different test cases.

In CPU(host) main function, the output buffer is copied to device, and it is written into “snapshot.bin” (via write_binarary_file() ).

Functional Requirements (90 points):

Implement fs_write operation (10 points)

Implement fs_read operation (10 points)

Implement fs_gsys(RM) operation (10 points)

Implement fs_gsys(LS_D) operation (10 points)

Implement fs_gsys(LS_S) operation (10 points)

Demo Output

There are four test cases In the “user_program.cu”.

Bonus (15 points)

In basic task, there is only one root directory for the file system. In bonus, you must implement tree-structured directories. (3 points)

A directory (or subdirectory) contains a set of files or subdirectories.

A directory is simply another file.

There are at most 50 files (include subdirectories) in a directory.

The size of a directory is the sum of character bytes of all files name (include subdirectories).

E.g., the directory root/ have these files:

“A.txt” “b.txt” “c.txt” “app”

The size of directory root/ is 22 bytes.

The maximum number of files (include directory) is 1024.

The maximum depth of the tree-structured directory is 3.

File operations: (12 points)

fs_gsys(fs, MKDIR, “app”); Create a directory named ‘app’. fs_gsys(fs, CD, “app”);

Enter app directory (only move to its subdirectory). fs_gsys(fs, CD_P);

Move up to parent directory. fs_gsys(fs, RM_RF, “app”);

Remove the app directory and all its subdirectories and files recursively. You cannot delete a directory by fs_gsys(fs, RM, “app”), cannot remove `app’ if it is a directory. fs, gsys(fs, PWD);

Print the path name of current, eg., “/app/soft”

fs_gsys(fs, LS_D / LS_S);

Update this file list operation, to list the files as well as directories. For a file, list it name (with size) only. For a directory, add an symbol ‘d’ at the end.

Demo test case:

/////////////////////// Bonus Test Case /////////////// u32 fp = fs_open(fs, “t.txt”, G_WRITE); fs_write(fs, input, 64, fp); fp = fs_open(fs, “b.txt”, G_WRITE); fs_write(fs, input + 32, 32, fp); fp = fs_open(fs, “t.txt”, G_WRITE); fs_write(fs, input + 32, 32, fp); fp = fs_open(fs, “t.txt”, G_READ); fs_read(fs, output, 32, fp); fs_gsys(fs, LS_D); fs_gsys(fs, LS_S); fs_gsys(fs, MKDIR, “app”); fs_gsys(fs, LS_D); fs_gsys(fs, LS_S); fs_gsys(fs, CD, “app”); fs_gsys(fs, LS_S);

fp = fs_open(fs, “a.txt”, G_WRITE); fs_write(fs, input + 128, 64, fp); fp = fs_open(fs, “b.txt”, G_WRITE); fs_write(fs, input + 256, 32, fp); fs_gsys(fs, MKDIR, “soft”); fs_gsys(fs, LS_S); fs_gsys(fs, LS_D); fs_gsys(fs, CD, “soft”); fs_gsys(fs, PWD);

fp = fs_open(fs, “A.txt”, G_WRITE); fs_write(fs, input + 256, 64, fp); fp = fs_open(fs, “B.txt”, G_WRITE); fs_write(fs, input + 256, 1024, fp); fp = fs_open(fs, “C.txt”, G_WRITE); fs_write(fs, input + 256, 1024, fp); fp = fs_open(fs, “D.txt”, G_WRITE); fs_write(fs, input + 256, 1024, fp); fs_gsys(fs, LS_S); fs_gsys(fs, CD_P); fs_gsys(fs, LS_S); fs_gsys(fs, PWD); fs_gsys(fs, CD_P); fs_gsys(fs, LS_S); fs_gsys(fs, CD, “app”); fs_gsys(fs, RM_RF, “soft”); fs_gsys(fs, LS_S); fs_gsys(fs, CD_P); fs_gsys(fs, LS_S);

Demo output:

Report (10 points)

Write a report for your assignment, which should include main information as below:

Environment of running your program. (E.g., OS, VS version, CUDA version, GPU information etc.)

Grading rules

Bonus 15 points

Report 10 points

Pass the additional grading cases 90

Pass test case 4 85+

Pass test case 3 79+

Pass test case 2 73+

Pass test case 1 67+

Fully Submitted (compile successfully) 60 +

Partial submitted 0 ~ 60

No submission 0
