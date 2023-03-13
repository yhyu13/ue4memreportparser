MemReport Parser
================
Parse UE4 MemReport files to see memory usage over time. For instance do a MemReport on
the Main Menu, load a level, go back to the Main Menu and do another MemReport. Repeat
as many times as you like. You can then spot any memory usage increase which would indicate
a memory or resource leak.

## Build
Use VS2019 or above to build this progrm.

## Usage

```
Parse UE4 MemReport files to see memory usage over time. For instance do a MemReport on
the Main Menu, load a level, go back to the Main Menu and do another MemReport. Repeat
as many times as you like. You can then spot any memory usage increase which would indicate
a memory or resource leak.

Usage:
  -i <input path> Specify the path where we search for .memreport files.
                  The folder should contain one or more .memreport files.

  -p <pattern>    File pattern to search for, can contain wildcards.
                  test-*.memreport
  -o <output directory> Specify the path where we output the csv.
  -stat           Calculate Min,Max,Avg and output them to csv along side values.
```

Example:

```
.\bin\Debug\MemReportParser.exe -i E:\...\GameProject\Saved\Profiling\MemReports\Windows-03.13-13.40.53 -o E:\...\GameProject\Saved\Profiling\MemReports\Windows-03.13-13.40.53\Output
```


# Python Ploting

We has modified this repo to support plotting memreport.

We recommand using Anaconda3 to install python environment.

```conda create -n ue4memreport python=3.10.6 -y```

```conda install pandas matplotlib jupyter notebook ipykernel -y```

Then run the notebook as below:

```jupyter-lab Plotmemreport.ipynb```