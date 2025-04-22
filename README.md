# STRING-Enrichment-from-Gene-CSV-using-STRING-db-API
<p>
This project allows you to perform <strong>automated functional enrichment analysis</strong> from a list of gene symbols in a CSV file, using the <a href="https://string-db.org/" target="_blank">STRING-db API</a>. It’s ideal for transcriptomics studies, gene panel analysis, and any high-throughput experiment requiring <strong>biological pathway interpretation</strong>.
</p>

<hr>

<h2>📂 Input File Format</h2>
<p>The input must be a simple CSV file named <code>gene-test.csv</code> (or renamed in code) with one header column named <code>Gene</code>:</p>

<pre>
Gene
TP53
EGFR
BRCA1
...
</pre>

<hr>

<h2>⚙️ How to Run</h2>
<ol>
  <li>Clone the repository:
    <pre><code>git clone https://github.com/shari01/string-enrichment-csv.git</code></pre>
  </li>
  <li>Navigate to the project folder:
    <pre><code>cd string-enrichment-csv</code></pre>
  </li>
  <li>Install required Python packages:
    <pre><code>pip install pandas requests</code></pre>
  </li>
  <li>Run the notebook:
    <pre><code>string_enrichment_from_csv.ipynb</code></pre>
  </li>
  <li>Edit the CSV filename if needed and run all cells.</li>
</ol>

<hr>

<h2>📈 Output Overview</h2>
<p>The tool maps gene symbols to STRING IDs and retrieves enriched pathways from several databases. The results are saved as tab-separated text files for each category.</p>

<h3>✅ Example Output:</h3>
<pre>
→ Read 146 genes from gene-test.csv
→ Mapped 141 STRING IDs
→ Retrieved enrichment from: KEGG, Reactome, WikiPathways, GO, HPO, Tissue, Disease

✅ biological_process.tsv (Gene Ontology)
✅ kegg.tsv (Main Pathways)
✅ rctm.tsv (Reactome)
✅ hpo.tsv (Phenotype)
✅ Saved all to enrichment_results/
</pre>

<h2>📁 Output Folder Structure</h2>
<pre>
📂 enrichment_results/
├── 📁 Gene_Ontology/
│   ├── biological_process.tsv
│   ├── molecular_function.tsv
│   └── compartments.tsv
├── 📁 Main-DB-pathways/
│   ├── kegg.tsv
│   ├── rctm.tsv
│   └── wikipathways.tsv
├── 📁 Other-Db-pathways/
│   ├── diseases.tsv
│   ├── tissues.tsv
│   ├── hpo.tsv
</pre>

<hr>

<h2>🔌 API Info</h2>
<p>This tool uses the official <a href="https://string-db.org/cgi/help?sessionId=bDJce52SGazF" target="_blank">STRING-db API</a> to:</p>
<ul>
  <li>Map gene symbols to STRING IDs</li>
  <li>Query enrichment for KEGG, Reactome, WikiPathways, GO (BP/MF/CC), HPO, Disease, and Tissue databases</li>
</ul>

<hr>

<h2>📌 Repo Name Suggestion</h2>
<p><strong>Repository:</strong> <code>string-enrichment-csv</code></p>

<h2>🙋‍♂️ Author</h2>
<p>
Developed by <a href="https://github.com/shari01" target="_blank">@shari01</a> — Feel free to fork, star ⭐, or open an issue for suggestions!
</p>

<hr>

<h2>📃 License</h2>
<p>This project is licensed under the <code>MIT License</code> — free for both academic and commercial use.</p>

<hr>

<h2>🙏 Contributions Welcome</h2>
<p>Pull requests, suggestions, and bug reports are appreciated. Let’s make this more powerful together!</p>
