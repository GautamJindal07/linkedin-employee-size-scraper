<h1>LinkedIn Employee Size Scraper</h1>

<p>
A Python-based Selenium automation script designed to extract employee-size
information from LinkedIn company pages and save the extracted data to CSV.
</p>

<h2>Overview</h2>

<p>
This project automates a repetitive company research task where employee-size
information is required for a set of companies.
</p>

<p>
The script reads LinkedIn company URLs from a CSV file, opens each page using
Selenium, waits for the required page element to load, extracts the displayed
text, and appends the URL and extracted value to an output CSV file.
</p>

<h2>Use Case</h2>

<p>
The script is useful when an exact employee-size value is required for a set
of companies during company research, prospecting, or data preparation.
</p>

<h2>Workflow</h2>

<p>
<strong>LinkedIn Company URLs</strong> →
<strong>Selenium + Chrome</strong> →
<strong>Open Company Page</strong> →
<strong>Locate Employee-Size Information</strong> →
<strong>Extract Value</strong> →
<strong>CSV Output</strong>
</p>

<h2>Technologies Used</h2>

<ul>
<li>Python</li>
<li>Selenium</li>
<li>Chrome WebDriver</li>
<li>CSV processing</li>
</ul>

<h2>Key Features</h2>

<ul>
<li>Processes multiple LinkedIn company URLs from a CSV file</li>
<li>Automates Chrome using Selenium</li>
<li>Waits for dynamically loaded page elements</li>
<li>Extracts text from a specified LinkedIn page element</li>
<li>Appends successful results to a CSV output file</li>
<li>Uses a single browser session for multiple URLs</li>
</ul>

<h2>Input</h2>

<p>
The input CSV contains a column named <strong>url</strong>. Each row contains
a LinkedIn company page URL.
</p>

<p>
A sample input file is included in the repository as
<strong>sample_input.csv</strong>.
</p>

<h2>Extraction Logic</h2>

<p>
The script waits for the configured CSS selector to become available and
then extracts the text from the matching element.
</p>

<p>The current extraction selector is:</p>

<pre>.artdeco-carousel__title.ember-view h2</pre>

<h2>Output</h2>

<p>
For each successfully processed URL, the script writes the source URL and
the extracted text to the output CSV.
</p>

<pre>
URL,Employee Size
LinkedIn company URL,Extracted employee-size value
</pre>

<h2>Scraping Approach</h2>

<ol>
<li>Read LinkedIn company URLs from the input CSV.</li>
<li>Open each URL using Selenium and Chrome.</li>
<li>Allow the page to load.</li>
<li>Wait for the configured page element.</li>
<li>Locate the matching element using its CSS selector.</li>
<li>Extract the text from the element.</li>
<li>Append the URL and extracted value to the output CSV.</li>
<li>Continue processing the remaining URLs.</li>
</ol>

<h2>Project Structure</h2>

<pre>
linkedin-employee-size-scraper/
│
├── employee_size.ipynb
├── sample_input.csv
├── requirements.txt
├── .gitignore
└── README.md
</pre>

<h2>Installation</h2>

<p>Install the required Python dependency:</p>

<pre>pip install -r requirements.txt</pre>

<h2>Usage</h2>

<ol>
<li>Place the input CSV in the same directory as the notebook.</li>
<li>Open <strong>employee_size.ipynb</strong> using Jupyter Notebook, JupyterLab, or VS Code with the Jupyter extension.</li>
<li>Run the notebook cells to process the LinkedIn company URLs.</li>
<li>The extracted employee-size information is appended to the configured output CSV.</li>
</ol>

<h2>Limitations</h2>

<p>
This workflow relies on an authenticated browser session and is subject to
LinkedIn's access controls and usage limitations. Automated activity should
be kept controlled, as excessive requests may trigger security restrictions
or account limitations.
</p>

<p>
LinkedIn page structures and CSS selectors can change over time. The
extraction selector may therefore need to be updated if the page structure
changes.
</p>

<h2>Privacy &amp; Security</h2>

<p>
Personal Chrome profile paths, authentication details, cookies, credentials,
or other private session information should not be included in a public
repository.
</p>

<h2>Notes</h2>

<p>
This project demonstrates browser automation and page-element based data
extraction for controlled employee-size research. It should be used
responsibly and in accordance with applicable website terms and policies.
</p>
