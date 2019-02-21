# Example code

This example code is all based on running an analysis using Amazon Web Services. You can start with the `SDSU Computational Genomics` AWS Image. To find this image, log into [AWS](https://aws.amazon.com) *[Note, you may need to create an account]*, click to launch a new EC2 instance, and then search the available public AMI's for SDSU Computational Genomics. A more thorough description is available in [this YouTube video](https://www.youtube.com/watch?v=s9E4Njfdib4).

# Example genome

For this work, we are going to use Pseudomonas phage PAK-P1, [available from RefSeq](https://www.ncbi.nlm.nih.gov/nuccore/NC_015294.2). The genome is 93,198 bp. You can download the genome in `fasta` format or `genbank` format using one of these two commands. *(Note, if you are not using a prebuilt image, you will need to install [eutils from NCBI](https://www.ncbi.nlm.nih.gov/books/NBK179288/) before using this command. See the [installation](Installation.md) documentation for more information.

```bash
esearch -db nuccore -query NC_015294 | efetch -format fasta > NC_015294.fasta
```
or
```bash
esearch -db nuccore -query NC_015294 | efetch -format gb > NC_015294.gbk
```

Note that both of these files are also present in the [data](data/) directory of the Git repository associated with this example.



