<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://launch.icarus2-scrnaseq.cloud.edu.au/">
    <img src="Images/ICARUS.png" alt="Logo" width="400" height="120">
  </a>

  <h3 align="center">ICARUS</h3>

  <p align="center">
    Interactive Single Cell RNA-seq Analysis Webserver!
    <br />
    <a href="#Changelog"><strong>See the changelog »</strong></a>
    <br />
    <br />
    ·
    <a href="https://github.com/Enjewl/ICARUS/issues">Report Bug</a>
    ·
    <a href="https://github.com/Enjewl/ICARUS/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#Accessing-ICARUS">Accessing ICARUS</a>
      <ul>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#Save-and-load-functionality">Save and load functionality</a></li>
    <li><a href="#changelog">Changelog</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project
Welcome to ICARUS (<b>I</b>nteractive single <b>C</b>ell RNA-seq <b>A</b>nalysis with <b>R</b> shiny <b>U</b>sing <b>S</b>eurat). <br> <br>
This application was designed to guide the user through single cell RNA-seq analysis using the <a href="https://www.satijalab.org/seurat/" target="_blank">Seurat scRNA-seq analysis toolkit</a> via a tutorial style interface. 
It offers user control over each of the steps to personalise analysis based on the dataset of interest. Graphical outputs at each analysis step ensures easy and logical interpretation.

The purpose of this application is to allow the user to interactively visualize single cell RNA-seq data without previous R programming knowledge.

Features include:
* Tutorial inspired user interface!
* Support for 11 common species!
* Apply your own cell quality control thresholds and remove cells with low quality (i.e. high mitochondrial percentage)!
* Removal of cell doublets (multiplets) with <a href="https://doi.org/10.1016/j.cels.2019.03.003" target="_blank">DoubletFinder</a>!
* Adjust your own dimensionality reduction and clustering parameters!
* 3D UMAP and t-SNE plots!
* Imputation of droupouts (false zeros in the dataset due to low amounts of mRNA in individual cells resulting in insufficient mRNA capture) using <a href="https://www.nature.com/articles/s41467-021-27729-z" target="_blank">Adaptively-thresholded low rank approximation (ALRA) method</a>
* Data correction for cell cycle effects!
* Labelling of cell clusters with <a href="https://doi.org/10.1038/s41467-022-28803-w" target="_blank">sctype</a> and <a href="https://doi.org/10.1038/s41590-018-0276-y" target="_blank">SingleR</a>!
* Gene expression and gene pathway visualisation!
* Gene co-expression analysis with <a href="https://doi.org/10.1371/journal.pcbi.1004574" target="_blank">MEGENA</a>!
* Gene regulatory network identification with <a href="https://doi.org/10.1038/nmeth.4463" target="_blank">SCENIC</a>!
* Examine cell cluster expression association with GWAS traits using <a href="https://doi.org/10.1371/journal.pcbi.1004219" target="_blank">MAGMA</a>!
* Trajectory analysis with <a href="https://doi.org/10.1038/nbt.2859" target="_blank">Monocle3</a>!
* Visualize and analyse cell-cell communication networks with <a href="https://doi.org/10.1038/s41467-021-21246-9" target="_blank">CellChat</a>!
* Examine drug-gene interactions of differentially expressed genes against the <a href="https://www.dgidb.org" target="_blank">DGIdb 4.0 database</a>!
* Differential expression analysis and gene set enrichment analysis with <a href="https://doi.org/10.1016/j.xinn.2021.100141" target="_blank">ClusterProfiler</a> and <a href="https://doi.org/10.1039/C5MB00663E" target="_blank">ReactomePA</a>
* Custom differential expression analysis with user selected cell groups to compare!
* Integration with second dataset and adjustment for batch effects!
* Support for multimodal analysis (i.e. CITE-seq, 10X multiome kit)!
* Save and continue functionality!
* Downloadable tables and plots!

### Built With

* [![Shiny][Shiny]][Shiny-url]
* [![Nectar][Nectar]][Nectar-url]

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Accessing ICARUS

The live version of ICARUS is available at <a href="https://launch.icarus-scrnaseq.cloud.edu.au/" target="_blank">https://launch.icarus-scrnaseq.cloud.edu.au/</a>. 
The test server with latest updates is available at <a href="https://launch.icarus2-scrnaseq.cloud.edu.au/" target="_blank">https://launch.icarus2-scrnaseq.cloud.edu.au/</a>. Please note that the test server utilises unpublised methodologies.

The application is free and open to all users with no login requirement. Alternatively, a docker version is accessible through the Docker Hub under the name ‘icarusscrnaseq/icarus’.

Source code is provided under the folder ICARUS_application/app.R 

**NOTE: Source code cannot be used to run ICARUS due to dependencies on several external files.**

### Installation

Requirements: Docker client

   ```sh
docker pull icarusscrnaseq/icarus:latest
docker run -p 8080:8080 icarusscrnaseq/icarus:latest
   ```

<!-- USAGE EXAMPLES -->
## Save and load functionality

ICARUS features local save and continue functionality. At each analysis step the user may opt to save their progress as a Rdata file containing the Seurat R object and the current working environment. 
The saved file can then be loaded at the CONTINUE interface at the ‘Introduction’ tab to resume analysis. <br>

Alternatively, the Seurat R object may be saved individually and loaded into R for a more in-depth analysis with a variety of supporting scRNA-seq analysis packages available in the R environment.

_For detailed list of saved objects, please refer to the [Documentation](https://github.com/Enjewl/ICARUS/blob/master/ICARUS_enviroment_descriptions.md)_

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CHANGELOG -->
## Changelog
<h4 class="mt-4"> <span class="p-2 bg-light shadow rounded text-success"> ICARUS Version 2.4</span> - 1st January, 2023</h4>
             <ul class="list-unstyled mt-3">
             <ul>
             <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW An option to impute dropouts using <a href="https://www.nature.com/articles/s41467-021-27729-z" target="_blank">Adaptively-thresholded low rank approximation (ALRA) method</a>.</li>
             </ul>
           </ul>
<h4 class="mt-4"> <span class="p-2 bg-light shadow rounded text-success"> ICARUS Version 2.3</span> - 18th October, 2022</h4>
             <ul class="list-unstyled mt-3">
             <ul>
             <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Improved search functionality for genes and gene pathways.</li>
                          <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW The height of ICARUS windows are now adjustable for many of the plots.</li>
                                       <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW A document describing the objects in the ICARUS enviroment is now <a href="https://github.com/Enjewl/ICARUS/blob/master/ICARUS_enviroment_descriptions.md" target="_blank">available</a> </li>
             </ul>
           </ul>

<h4 class="mt-4"> <span class="p-2 bg-light shadow rounded text-success"> ICARUS Version 2.2</span> - 11th June, 2022</h4>
             <ul class="list-unstyled mt-3">
             <ul>
             <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Analyze gene Co-expression with MEGENA, read more about it <a href="https://doi.org/10.1371/journal.pcbi.1004574" target="_blank">here</a>.</li>
                          <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Analyze gene regulatory networks from transcription factors and target genes with SCENIC, read more about it <a href="https://doi.org/10.1038/nmeth.4463" target="_blank">here</a>.</li>
                                       <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Examine cell cluster expression association with various Genome Wide Association Studies (GWAS) traits using MAGMA, read more about it <a href="https://doi.org/10.1371/journal.pcbi.1004219" target="_blank">MAGMA</a>.</li>
                                                    <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Visualize and analyze cell-cell communication networks (ligand-receptor interactions between cells) with CellChat, read more about it <a href="https://doi.org/10.1038/s41467-021-21246-9" target="_blank">here</a>.</li>
                                                                                                                                                            <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Examine drug-gene interactions of differentially expressed genes against the <a href="https://www.dgidb.org" target="_blank">DGIdb 4.0 database</a>!</li>
             </ul>
           </ul>
      
<h4 class="mt-4"> <span class="p-2 bg-light shadow rounded text-success"> ICARUS Version 2.1</span> - 10th May, 2022</h4>
             <ul class="list-unstyled mt-3">
             <ul>
             <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>ICARUS is now published in <a href="https://doi.org/10.1093/nar/gkac322" target="_blank">Nucleic Acids Research!</a></li>
             </ul>
           </ul>
           
<h4 class="mt-4"> <span class="p-2 bg-light shadow rounded text-success"> ICARUS Version 2.0 </span> - 21st April, 2022</h4>
            <ul class="list-unstyled mt-3"> 
            <ul>
            <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Perform trajectory analysis with <b>Monocle3</b>, read more about it <a href="https://doi.org/10.1038/nbt.2859" target="_blank">here</a>.</li>
            <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Detection and removal of doublets in data with <b>DoubletFinder</b>, read more about it <a href="https://doi.org/10.1016/j.cels.2019.03.003" target="_blank">here</a>.</li>
            <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Cell cluster labelling with <b>sctype</b>. The <a href="https://doi.org/10.1038/s41467-022-28803-w" target="_blank">sctype reference dataset</a> compiled cell markers from 
                  <a href="http://bio-bigdata.hrbmu.edu.cn/CellMarker/" target="_blank">CellMarker</a> and 
                  <a href="https://panglaodb.se/" target="_blank">PanglaoDB</a> databases and includes markers for the brain, pancreas, immune system, liver, eye, kidney, lung, embryo, gastrointestinal tract, muscle and skin.</li>
            <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>NEW Reference datasets for cell labelling with <b>SingleR</b>. These include: <br>
                  <b>Brain</b>
                  <ul><li>Darmanis Brain Data: scRNA-seq of 8 adult and 4 fetal human brain temporal lobe tissue (<a href="https://doi.org/10.1073/pnas.1507125112" target="_blank">Darmanis et al., 2015</a>). </li>
                  <li>Zhong Prefrontal Cortex Data: scRNA-seq of developing human embryonic prefrontal cortex from gestational weeks 8 to 26 (<a href="https://doi.org/10.1038/nature25980" target="_blank">Zhong et al., 2018</a>). </li></ul>
                  <b>Pancreas</b><br>
                          <ul><li>Baron Pancreas Data: scRNA-seq of pancreatic cells from 4 human donors and 2 mouse strains (<a href="https://doi.org/10.1016/j.cels.2016.08.011" target="_blank">Baron et al., 2016</a>). </li>
                          <li>Lawlor Pancreas Data: scRNA-seq of 5 non-diabetic and 8 type 2 diabetic human islet samples (<a href="https://doi.org/10.1101/gr.212720.116" target="_blank">Lawlor et al., 2017</a>). </li>
                          <li>Muraro Pancreas Data: scRNA-seq of pancreatic cells from 4 human donors (<a href="https://doi.org/10.1016/j.cels.2016.09.002" target="_blank">Muraro et al., 2016</a>). </li>
                          <li>Segerstolpe Pancreas Data: scRNA-seq of human islet cells from 6 healthy and 4 type 2 diabetic donors (<a href="https://doi.org/10.1016/j.cmet.2016.08.020" target="_blank">Segerstolpe et al., 2016</a>). </li></ul>
                  <b>Multiple organs</b>        
                          <ul><li>He Organ Atlas: scRNA-seq of 15 tissue organs of one adult donor. Tissue organs include bladder, blood, common bile duct, oesophagus, heart, liver,
                          lymph node, bone marrow, muscle, rectum, skin, small intestine, spleen, stomach and trachea 
                          (<a href="https://doi.org/10.1186/s13059-020-02210-0" target="_blank">He et al., 2020</a>).</li></ul>
             </li>
             </ul>
             </ul>

<h4 class="mt-4"> <span class="p-2 bg-light shadow rounded text-success"> ICARUS Version 1.0</span> - 15th March, 2022</h4>
             <ul class="list-unstyled mt-3">
             <ul>
             <li class="text-muted ml-3"><i class="mdi mdi-circle-medium mr-2"></i>Initial Release</li>
             </ul>
           </ul>

See the [open issues](https://github.com/Enjewl/ICARUS/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are greatly appreciated. 
To report any bugs or suggest new features, please log an issue through the issue tracker. For direct inquiries, please send an email to ajia169@aucklanduni.ac.nz

<!-- CITATION -->
## Citation

If you used ICARUS for your research, please cite the following publication:

Jiang, A., Lehnert, K., You, L. and Snell, R.G. (2022) ICARUS, an interactive web server for single cell RNA-seq analysis. Nucleic Acids Research. https://doi.org/10.1093/nar/gkac322

Where applicable, please also cite the relevant R package(s) that ICARUS draws functionality from.

<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<!-- CONTACT -->
## Contact

Andrew Jiang - [@Andrew_Jiang_NZ](https://twitter.com/Andrew_Jiang_NZ) - ajia169@aucklanduni.ac.nz

Project Link: [https://github.com/Enjewl/ICARUS/](https://github.com/Enjewl/ICARUS/)


<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

ICARUS functionality is based on the [Seurat single cell RNA-seq toolkit ](https://satijalab.org/seurat/)

ICARUS additionally incorporates functionality from the following R packages:
* <a href="https://github.com/chris-mcginnis-ucsf/DoubletFinder" target="_blank">DoubletFinder</a> 
* <a href="https://github.com/KlugerLab/ALRA" target="_blank">ALRA</a> 
* <a href="https://github.com/IanevskiAleksandr/sc-type" target="_blank">sctype</a>
* <a href="https://bioconductor.org/packages/release/bioc/html/SingleR.html" target="_blank">SingleR</a>
* <a href="https://github.com/songw01/MEGENA" target="_blank">MEGENA</a>
* <a href="https://github.com/aertslab/SCENIC" target="_blank">SCENIC</a>
* <a href="https://github.com/neurogenomics/MAGMA_Celltyping" target="_blank">MAGMA.celltyping</a>
* <a href="https://github.com/cole-trapnell-lab/monocle3" target="_blank">Monocle3</a>
* <a href="https://github.com/sqjin/CellChat" target="_blank">CellChat</a>
* <a href="https://github.com/YuLab-SMU/clusterProfiler" target="_blank">ClusterProfiler</a>
* <a href="https://github.com/YuLab-SMU/ReactomePA" target="_blank">ReactomePA</a>
* <a href="https://www.dgidb.org" target="_blank">DGIdb 4.0 database</a>

A big thank you to [Nectar Research Cloud](https://ardc.edu.au/services/ardc-nectar-research-cloud/) for hosting the webserver!

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[Shiny]: https://img.shields.io/badge/Shiny-03d7fc?style=for-the-badge&logo=R&logoColor=blue
[Shiny-url]: https://shiny.rstudio.com/
[Nectar]: https://img.shields.io/badge/Nectar%20research%20cloud-e3fc03?style=for-the-badge
[Nectar-url]: https://ardc.edu.au/services/ardc-nectar-research-cloud/
