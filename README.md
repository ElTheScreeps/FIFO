FIFO (First in First out):

![FIFO Diagram](https://github.com/ElTheScreeps/FIFO/assets/115155585/6b6a5e19-9899-413f-a542-6386f4c5784c)

| Name        | Parameter   | Value  | Default | Value Range       | Description                                                          |
|-------------|-------------|--------|---------|-------------------|----------------------------------------------------------------------|
| DATA_WIDTH  | 8 >= 1      |        |         |                   | Size of the data                                                     |
| ADDR_WIDTH  | 4 > 1       |        |         |                   | Size of the internal address. Determines the FIFO depth (2^ADDR WIDTH|

| Port Name   | Direction   | Size       | Description                                                            |
|-------------|-------------|------------|------------------------------------------------------------------------|
| clk         | IN          | 1          | Clock signal                                                           |
| rst_n       | IN          | 1          | Asynchronous reset signal, active low                                  |
| push        | IN          | 1          | Write command for data, valid only if the memory is not full (full=0)  |
| data_in     | IN          | DATA_WIDTH | Written data                                                           |
| pop         | IN          | 1          | Read command for data, valid only if the memory is not empty (empty=0) |
| data_out    | OUT         | DATA_WIDTH | Read data (first written)                                              |
| empty       | OUT         | 1          | FIFO memory empty indicator. No reads (pop) are allowed                |
| full        | OUT         | 1          | FIFO memory full indicator. No writes (push) are allowed               |


How to use this files:

1. Download the files;
2. Put them in a directory;
3. Open Modelsim;
4. Change directory to the directory who contain the files;
5. Create a project and add the files;
6. Compile the files and start stimulate.
