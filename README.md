# build fgwas input file (01 script) 

## **Note:** You must manually format your gwas data file into a "bed" type format with no header and the first 3 columns must be chromosome, start position, end position, the rest you can include to fit your needs (i.e. whole gwas or regions of interest i.e. credible sets) 

Here is an example of the format:

chr1	693730	693731	chr1:693731	0.8795	0.08	0.9362	47440	463435
chr1	729678	729679	chr1:729679	0.1663	-0.28	0.7794	47291	461541
...

Note that the convention you use for chromosome must be consistent between bed files 

## Arguments 

**bedtools**:  Path to executable bedtools program 

**cur_dir**: Your current work diretory (i.e. fgwas_input/) 

**fgwas_head_list**: A python list of the fgwas column names for the gwas fields you will have in the final fgwas input file, here is an example: 

["CHR","POS0","POS","SNPID","F","Z","PVAL","NCASE","NCONTROL"]


**annot_bed_file**: Path to annotation bed file (you must prepare to suit your needs) 

**gwas_bed_file**: Path to the gwas bed file (you must prepare, see previous section) 



# fgwas_wrappers (02 scripts) 
Run fGWAS recommended pipeline on server

## Configure "global" section of fgwas_wrapper_genome-wide.py 

* **fgwas**: path to fgwas exectutable file # test in screen if you decide to run in background (RECOMMENDED)

* **in_dir**: path to fgwas input file directory 

* **out_dir**: path to fgwas output directory 

* **input_file**: name of fgwas input file in in_dir 

* **start_index**: 0-based index of first column in fgwas input file where annotations begin

* **home_dir**: working directory 


