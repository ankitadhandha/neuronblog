<style> body { margin: 0; } </style>
 <script src="//unpkg.com/three"></script>
  <script src="//unpkg.com/three-spritetext"></script>
  <script src="//unpkg.com/element-resize-detector/dist/element-resize-detector.min.js"></script>
  <script src="//unpkg.com/3d-force-graph"></script>
 
 
  
<script src="https://unpkg.com/three@0.119.1/build/three.js"></script>
<script src="https://unpkg.com/three-spritetext@1.5.2/dist/three-spritetext.min.js"></script>
<script src="https://unpkg.com/3d-force-graph@1.66.6/dist/3d-force-graph.min.js"></script>

<title>
Knowledge Graph: Ontomatica
</title>

</head>
<body>

<div id="3d-graph"></div>

<div class="filtresX">
Knowledge Graph: Ontomatica
</div>

<div class="rightside-buttons">
<div class="recenter" onClick="Graph.cameraPosition({ x: 0, y: 0, z: 800 }, { x: 0, y: 0, z: 0 }, 2000);"></div>
</div>

<script>

const Graph = ForceGraph3D()
(document.getElementById("3d-graph"))
//.jsonUrl("https://benetta.io/graph/fdg-1/data.json")
.jsonUrl("https://afdsi.com/data/onto-id-v3/data.json")

// NODES
.nodeLabel("name")
//.nodeAutoColorBy("group")
.nodeVal("value")
.nodeResolution("20")

.nodeColor(d => {

if (d.name === "@Intangible"){return "#D1D5DB";}
else if (d.name === "Audience"){return "#93a806";}
else if (d.name === "Enumeration"){return "#78350F";}
else if (d.name === "Health Aspect Enumeration"){return "#D97706";}
else if (d.name === "Medical Enumeration"){return "#D97706";}
else if (d.name === "Nonprofit Type"){return "#D97706";}
else if (d.name === "US Nonprofit Type"){return "#FCD34D";}
else if (d.name === "501C3"){return "#FDE68A";}
else if (d.name === "Restricted Diet"){return "#D97706";}
else if (d.name === "Language"){return "#36688d";}
else if (d.name === "Offer"){return "#0000ff";}
else if (d.name === "Price Specification"){return "#0E7490";}
else if (d.name === "Quantitative Value"){return "#06B6D4";}
else if (d.name === "Service"){return "#D97706";}
else if (d.name === "WebAPI"){return "#FCD34D";}
else if (d.name === "Structured Value"){return "#78350F";}
else if (d.name === "Nutrition Information"){return "#D97706";}
else if (d.name === "Specialty"){return "#701A75";}
else if (d.name === "Warranty Promise"){return "#9CA3AF";}
else if (d.name === "Agriculture Profession"){return "#bed905";}
else if (d.name === "Agricultural Engineers"){return "#dbb4da";}
else if (d.name === "Agricultural Inspectors"){return "#dbb4da";}
else if (d.name === "Animal Breeders"){return "#dbb4da";}
else if (d.name === "Animal Scientists"){return "#dbb4da";}
else if (d.name === "Farming and Fishing Occupations"){return "#dbb4da";}
else if (d.name === "Pesticide Handlers; Sprayers; and Applicators, Vegetation"){return "#dbb4da";}
else if (d.name === "Soil and Plant Scientists"){return "#dbb4da";}
else if (d.name === "Veterinarians"){return "#dbb4da";}
else if (d.name === "Veterinary Technologists and Technicians"){return "#dbb4da";}
else if (d.name === "Food Processing Profession"){return "#bed905";}
else if (d.name === "Bakers"){return "#dbb4da";}
else if (d.name === "Butchers and Meat Cutters"){return "#dbb4da";}
else if (d.name === "Food Batchmakers"){return "#dbb4da";}
else if (d.name === "Food Preparation and Serving Related Occupations"){return "#dbb4da";}
else if (d.name === "Food Scientists and Technologists"){return "#dbb4da";}
else if (d.name === "Slaughterers and Meat Packers"){return "#dbb4da";}
else if (d.name === "Chemical Creation Profession"){return "#bed905";}
else if (d.name === "Chemical Engineers"){return "#dbb4da";}
else if (d.name === "Chemists"){return "#dbb4da";}
else if (d.name === "Information Management Profession"){return "#bed905";}
else if (d.name === "Curators"){return "#dbb4da";}
else if (d.name === "Interpreters and Translators"){return "#dbb4da";}
else if (d.name === "Human Health Profession"){return "#bed905";}
else if (d.name === "Bioengineers and Biomedical Engineers"){return "#dbb4da";}
else if (d.name === "Biochemists and Biophysicists"){return "#dbb4da";}
else if (d.name === "Dietitians and Nutritionists"){return "#dbb4da";}
else if (d.name === "Epidemiologists"){return "#dbb4da";}
else if (d.name === "Life, Physical, and Social Science Occupations"){return "#dbb4da";}
else if (d.name === "Medical and Clinical Laboratory Technologists"){return "#dbb4da";}
else if (d.name === "Medical Records Specialists"){return "#dbb4da";}
else if (d.name === "Medical Scientists"){return "#dbb4da";}
else if (d.name === "Microbiologists"){return "#dbb4da";}
else if (d.name === "Pharmacists"){return "#dbb4da";}
else if (d.name === "Animal Science and Animal Products"){return "#F0ABFC";}
else if (d.name === "Biological Sciences"){return "#F0ABFC";}
else if (d.name === "Breeding and Genetic Improvement"){return "#F0ABFC";}
else if (d.name === "Food and Human Nutrition"){return "#F0ABFC";}
else if (d.name === "Health and Pathology"){return "#F0ABFC";}
else if (d.name === "Insects and Entomology"){return "#F0ABFC";}
else if (d.name === "Natural Resources, Earth and Environment"){return "#F0ABFC";}
else if (d.name === "Physical and Chemical Sciences"){return "#F0ABFC";}
else if (d.name === "Plant Science and Plant Products"){return "#F0ABFC";}
else if (d.name === "Taxonomic Classification of Organisms"){return "#F0ABFC";}
else if (d.name === "Information Technology, Data Engineering"){return "#F0ABFC";}
else if (d.name === "Information Product"){return "#ee6c81";}
else if (d.name === "Data Kit"){return "#192e5b";}
else if (d.name === "Substance Data Kit"){return "#720017";}
else if (d.name === "Product Data Kit"){return "#d8d583";}
else if (d.name === "Chemical Product Data Kit"){return "#f3d480";}
else if (d.name === "Food Product Data Kit"){return "#f3d480";}
else if (d.name === "Drug Product Data Kit"){return "#f3d480";}
else if (d.name === "Cosmetics Product Data Kit"){return "#f3d480";}
else if (d.name === "Textile Product Data Kit"){return "#f3d480";}
else if (d.name === "Linked Data Indexing"){return "#192e5b";}
else if (d.name === "Knowledge Graph Kit"){return "#192e5b";}
else if (d.name === "Agriculture Graph Kit"){return "#55d9c0";}
else if (d.name === "Aquaculture Graph Kit"){return "#c7f6ec";}
else if (d.name === "Product Identity Graph Kit"){return "#107050";}
else if (d.name === "Food, Drink & Meal Graph Kit"){return "#02231c";}
else if (d.name === "Sensory Science Graph Kit"){return "#4dd8ad";}
else if (d.name === "Human Health Graph Kit"){return "#0444bf";}
else if (d.name === "Product Safety Graph Kit"){return "#0584f2";}
else if (d.name === "Regulation & Trade Graph Kit"){return "#0aaff1";}
else if (d.name === "Consumer Service Graph Kit"){return "#edf259";}
else if (d.name === "Public Service & Research Graph Kit"){return "#a79674";}
else if (d.name === "Product Design & Development Graph Kit"){return "#f09285";}
else if (d.name === "Graph Application"){return "#728ca3";}
else if (d.name === "Web Enabled Directed Graph Engine"){return "#73c0f4";}
else if (d.name === "Graph Analysis"){return "#f3e46c";}
else if (d.name === "Electronic Product"){return "#0584f2";}
else if (d.name === "Electronic Label"){return "#0aaff1";}
else if (d.name === "Electronic Record"){return "#edf259";}
else if (d.name === "Electronic Biography"){return "#a79674";}
else if (d.name === "Electronic Commerce"){return "#a3586d";}
else if (d.name === "Electronic Product Passport"){return "#574a72";}
else if (d.name === "Electronic Border Control"){return "#f3b05a";}
else if (d.name === "Machine Automation Product"){return "#93a806";}
else if (d.name === "Machine Reasoning and Learning Product"){return "#bed905";}
else if (d.name === "Legacy Migration Product"){return "#012172";}
else if (d.name === "Development Product"){return "#ee6c81";}
else if (d.name === "Platform for Ontology"){return "#23345c";}
else if (d.name === "Plato Toolchain"){return "#f1ba48";}
else if (d.name === "Item Markup Language - Linked Data"){return "#f1ba48";}
else if (d.name === "Python Development Environment"){return "#5398d9";}
else if (d.name === "Python tools"){return "#d96b03";}
else if (d.name === "PyThing"){return "#d96b03";}
else if (d.name === "Chemical Entities of Food Significance"){return "#73c0f4";}
else if (d.name === "Chemical Entities with Medical Applications, Therapeutic Indications and Consequences"){return "#b5b3be";}
else if (d.name === "Dietary Data Reference"){return "#f3e46c";}
else if (d.name === "Food Data Kit"){return "#b5b3be";}
else if (d.name === "Vocal"){return "#f3e46c";}
else if (d.name === "Glucosinolates Research"){return "#b5b3be";}
else if (d.name === "Homeopathic Remedies"){return "#f3e46c";}
else if (d.name === "Reference Library"){return "#b5b3be";}
else if (d.name === "Specialty Foods"){return "#f3e46c";}
else if (d.name === "Dietary Supplements"){return "#b5b3be";}
else if (d.name === "USDA Food and Nutrient Database for Dietary Studies"){return "#f3e46c";}
else if (d.name === "USDA Standard Reference"){return "#b5b3be";}
else if (d.name === "Graph Visualization"){return "#be7052";}
else if (d.name === "Graph Analytics"){return "#f1ded1";}
else if (d.name === "Afro-Asiatic languages"){return "#bda589";}
else if (d.name === "Arabic"){return "#f49f05";}
else if (d.name === "Austro-Asiatic languages"){return "#bda589";}
else if (d.name === "Khmer"){return "#f49f05";}
else if (d.name === "Vietnamese"){return "#f49f05";}
else if (d.name === "Austronesian languages"){return "#bda589";}
else if (d.name === "Malay"){return "#f49f05";}
else if (d.name === "Dravidian languages"){return "#bda589";}
else if (d.name === "Telugu"){return "#f49f05";}
else if (d.name === "Sino-Tibetan languages"){return "#bda589";}
else if (d.name === "Burmese"){return "#f49f05";}
else if (d.name === "Chinese"){return "#f49f05";}
else if (d.name === "Indo-European languages"){return "#bda589";}
else if (d.name === "Czech"){return "#f49f05";}
else if (d.name === "English"){return "#f49f05";}
else if (d.name === "English Great Britain"){return "#f3cd05";}
else if (d.name === "English United States"){return "#f3cd05";}
else if (d.name === "French"){return "#f49f05";}
else if (d.name === "German"){return "#f49f05";}
else if (d.name === "Hindi"){return "#f49f05";}
else if (d.name === "Italian"){return "#f49f05";}
else if (d.name === "Persian"){return "#f49f05";}
else if (d.name === "Polish"){return "#f49f05";}
else if (d.name === "Portuguese"){return "#f49f05";}
else if (d.name === "Romanian"){return "#f49f05";}
else if (d.name === "Russian"){return "#f49f05";}
else if (d.name === "Slovak"){return "#f49f05";}
else if (d.name === "Spanish"){return "#f49f05";}
else if (d.name === "Swedish"){return "#f49f05";}
else if (d.name === "Ukrainian"){return "#f49f05";}
else if (d.name === "Japonic languages"){return "#bda589";}
else if (d.name === "Japanese"){return "#f49f05";}
else if (d.name === "Koreanic languages"){return "#bda589";}
else if (d.name === "Korean"){return "#f49f05";}
else if (d.name === "Ibero-Caucasian languages"){return "#bda589";}
else if (d.name === "Georgian"){return "#f49f05";}
else if (d.name === "Kra-Dai languages"){return "#bda589";}
else if (d.name === "Lao"){return "#f49f05";}
else if (d.name === "Thai"){return "#f49f05";}
else if (d.name === "Turkic languages"){return "#bda589";}
else if (d.name === "Turkish"){return "#f49f05";}
else if (d.name === "Uralic languages"){return "#bda589";}
else if (d.name === "Hungarian"){return "#f49f05";}
else if (d.name === "Ontology"){return "#006400";}
else if (d.name === "Biology-and-Chemistry"){return "#008b8b";}
else if (d.name === "Biochemistry"){return "#00fa9a";}
else if (d.name === "Genotype"){return "#00fa9a";}
else if (d.name === "Health"){return "#00fa9a";}
else if (d.name === "Phenotype"){return "#00fa9a";}
else if (d.name === "Protein"){return "#00fa9a";}
else if (d.name === "Research-Analysis-Methods"){return "#00fa9a";}
else if (d.name === "Species"){return "#00fa9a";}
else if (d.name === "Education"){return "#008b8b";}
else if (d.name === "Career-Description"){return "#00fa9a";}
else if (d.name === "Skill-Competence"){return "#00fa9a";}
else if (d.name === "Training"){return "#00fa9a";}
else if (d.name === "Finance-and-Trade"){return "#008b8b";}
else if (d.name === "Finance"){return "#00fa9a";}
else if (d.name === "Trade"){return "#00fa9a";}
else if (d.name === "Transportation"){return "#00fa9a";}
else if (d.name === "Food-and-Nutrition"){return "#008b8b";}
else if (d.name === "Agriculture"){return "#00fa9a";}
else if (d.name === "Commodity"){return "#00fa9a";}
else if (d.name === "Food-Composition"){return "#00fa9a";}
else if (d.name === "Food-Quality"){return "#00fa9a";}
else if (d.name === "Food-Safety"){return "#00fa9a";}
else if (d.name === "Food-Specification"){return "#00fa9a";}
else if (d.name === "Nutrition"){return "#00fa9a";}
else if (d.name === "Government-and-Regulation"){return "#008b8b";}
else if (d.name === "European-Union"){return "#00fa9a";}
else if (d.name === "United-Nations"){return "#00fa9a";}
else if (d.name === "United-States"){return "#00fa9a";}
else if (d.name === "Information-Technology"){return "#008b8b";}
else if (d.name === "Archival-Science"){return "#00fa9a";}
else if (d.name === "Data-Processing"){return "#00fa9a";}
else if (d.name === "Security"){return "#00fa9a";}
else if (d.name === "Software"){return "#00fa9a";}
else if (d.name === "Supply-Chain"){return "#00fa9a";}
else if (d.name === "Lexicon-and-Relations"){return "#008b8b";}
else if (d.name === "Lexicon"){return "#00fa9a";}
else if (d.name === "National-Language"){return "#00fa9a";}
else if (d.name === "Relations"){return "#00fa9a";}
else if (d.name === "Measurement-and-Statistics"){return "#008b8b";}
else if (d.name === "Information-Artifact"){return "#00fa9a";}
else if (d.name === "Measurement"){return "#00fa9a";}
else if (d.name === "Statistics"){return "#00fa9a";}
else if (d.name === "Sensor-and-Automation"){return "#008b8b";}
else if (d.name === "Agriculture-Automation"){return "#00fa9a";}
else if (d.name === "Machine-Control"){return "#00fa9a";}
else if (d.name === "Machine-Learning"){return "#00fa9a";}
else if (d.name === "Sensors"){return "#00fa9a";}
else if (d.name === "Space-and-Time"){return "#008b8b";}
else if (d.name === "Space-Climate"){return "#00fa9a";}
else if (d.name === "Space-Environment-Science"){return "#00fa9a";}
else if (d.name === "Space-Geography"){return "#00fa9a";}
else if (d.name === "Space-Soil"){return "#00fa9a";}
else if (d.name === "Space-Species"){return "#00fa9a";}
else if (d.name === "Time"){return "#00fa9a";}
else if (d.name === "Amino Acids"){return "#9acd32";}
else if (d.name === "Chemical Entities of Biological Interest"){return "#9acd32";}
else if (d.name === "Food Additive Biochemistry"){return "#9acd32";}
else if (d.name === "Food Contact Material Biochemistry"){return "#9acd32";}
else if (d.name === "Food Nutrient Biochemistry"){return "#9acd32";}
else if (d.name === "Food Protection Biochemistry"){return "#9acd32";}
else if (d.name === "Human Pathways"){return "#9acd32";}
else if (d.name === "Lipids"){return "#9acd32";}
else if (d.name === "Organoleptic Biochemistry"){return "#9acd32";}
else if (d.name === "Gene Ontology"){return "#9acd32";}
else if (d.name === "Drug Ontology"){return "#9acd32";}
else if (d.name === "US NIH Medical Subject Headings"){return "#9acd32";}
else if (d.name === "Integrated Taxonomic Information System"){return "#9acd32";}
else if (d.name === "GS1 Ontology"){return "#3cb371";}
else if (d.name === "Fish Ontology"){return "#7cfc00";}
else if (d.name === "US FDA SPL"){return "#0000ff";}
else if (d.name === "Provenance Ontology"){return "#ffd700";}
else if (d.name === "US Library of Congress Subject Headings"){return "#ffd700";}
else if (d.name === "Information Classes"){return "#0000ff";}
else if (d.name === "Information Types"){return "#0000ff";}
else if (d.name === "ISO 11238"){return "#eee8aa";}
else if (d.name === "Web Ontology Language"){return "#eee8aa";}
else if (d.name === "Resource Description Framework (RDF)"){return "#eee8aa";}
else if (d.name === "Schema.org"){return "#eee8aa";}
else if (d.name === "Simple Knowledge Organization System"){return "#eee8aa";}
else if (d.name === "UN FAO AGROVOC"){return "#eee8aa";}
else if (d.name === "USDA National Agricultural Library Thesaurus"){return "#eee8aa";}
else if (d.name === "US NIH NCI Thesaurus"){return "#eee8aa";}
else if (d.name === "Lexicon Model for Ontologies"){return "#eee8aa";}
else if (d.name === "Relations Ontology"){return "#dda0dd";}
else if (d.name === "Wikimedia Wikidata"){return "#dda0dd";}
else if (d.name === "Blood Glucose Monitoring Ontology"){return "#dcdcdc";}
else if (d.name === "Semantic Sensor Network Ontology"){return "#dcdcdc";}
else if (d.name === "Life Cycle Analysis Ontology"){return "#8fbc8f";}
else if (d.name === "Soil Chemistry Ontology US DOI US GS"){return "#808000";}
else if (d.name === "Soil Composition Ontology"){return "#808000";}
else if (d.name === "Technology"){return "#8f4f06";}
else if (d.name === "Information Technologies"){return "#73c0f4";}
else if (d.name === "Graph Format"){return "#5aa382";}
else if (d.name === "Knowledge Format"){return "#78d68c";}
else if (d.name === "Definition & Documentation"){return "#bda728";}
else if (d.name === "Graph Validation"){return "#704307";}
else if (d.name === "Graph Query"){return "#f7b178";}
else if (d.name === "Graph Visualization"){return "#253f5b";}
else if (d.name === "Natural Language Format"){return "#4f728e";}
else if (d.name === "Data Storage Format"){return "#be8260";}
else if (d.name === "Development Environment"){return "#d7b095";}
else if (d.name === "Web Format"){return "#74412b";}
else if (d.name === "Infrastructure"){return "#777ca8";}
else if (d.name === "Wearable Technology"){return "#73c0f4";}
else if (d.name === "Agriculture Technology"){return "#3cb371";}
else if (d.name === "Resource Description Framework"){return "#5aa382";}
else if (d.name === "JSON-LD"){return "#5aa382";}
else if (d.name === "Web Ontology Language"){return "#78d68c";}
else if (d.name === "Description Logic"){return "#78d68c";}
else if (d.name === "Protege"){return "#bda728";}
else if (d.name === "Sphinx"){return "#bda728";}
else if (d.name === "Linked Open Data Environment"){return "#bda728";}
else if (d.name === "Neuron"){return "#bda728";}
else if (d.name === "Structured Data Linter"){return "#704307";}
else if (d.name === "Structured Data Testing Tool"){return "#704307";}
else if (d.name === "Shape Constraints Language"){return "#704307";}
else if (d.name === "SPARQL"){return "#f7b178";}
else if (d.name === "Faceted Search"){return "#f7b178";}
else if (d.name === "Web Enables Directed Graph Engine"){return "#253f5b";}
else if (d.name === "Data Driven Documents"){return "#253f5b";}
else if (d.name === "Unicode"){return "#4f728e";}
else if (d.name === "Notation 3"){return "#be8260";}
else if (d.name === "Triplestore"){return "#be8260";}
else if (d.name === "MySQL"){return "#be8260";}
else if (d.name === "Python"){return "#d7b095";}
else if (d.name === "Haskell"){return "#d7b095";}
else if (d.name === "Javascript"){return "#d7b095";}
else if (d.name === "Accelerated Mobile Page"){return "#74412b";}
else if (d.name === "Amazon Web Services"){return "#777ca8";}
else if (d.name === "@Place"){return "#74412b";}
else if (d.name === "Africa"){return "#A0522D";}
else if (d.name === "Africa, Eastern"){return "#a37c27";}
else if (d.name === "Kenya"){return "#a37c27";}
else if (d.name === "Africa, Northern"){return "#a37c27";}
else if (d.name === "Egypt"){return "#a37c27";}
else if (d.name === "Africa, Southern"){return "#a37c27";}
else if (d.name === "South Africa"){return "#a37c27";}
else if (d.name === "Asia"){return "#A0522D";}
else if (d.name === "Asia, Northeast"){return "#a37c27";}
else if (d.name === "China, Peoples Republic Of"){return "#a37c27";}
else if (d.name === "China, Republic Of"){return "#a37c27";}
else if (d.name === "Hong Kong"){return "#a37c27";}
else if (d.name === "Japan"){return "#a37c27";}
else if (d.name === "Korea, Republic Of"){return "#a37c27";}
else if (d.name === "Asia, Southeast"){return "#a37c27";}
else if (d.name === "Singapore"){return "#a37c27";}
else if (d.name === "Asia, Southern"){return "#a37c27";}
else if (d.name === "India"){return "#a37c27";}
else if (d.name === "Asia, Western"){return "#a37c27";}
else if (d.name === "Pakistan"){return "#a37c27";}
else if (d.name === "Middle East"){return "#a37c27";}
else if (d.name === "Israel"){return "#a37c27";}
else if (d.name === "Kuwait"){return "#a37c27";}
else if (d.name === "Qatar"){return "#a37c27";}
else if (d.name === "Saudi Arabia"){return "#a37c27";}
else if (d.name === "Turkey"){return "#a37c27";}
else if (d.name === "United Arab Emirates"){return "#a37c27";}
else if (d.name === "Australia"){return "#A0522D";}
else if (d.name === "Central America"){return "#A0522D";}
else if (d.name === "Costa Rica"){return "#a37c27";}
else if (d.name === "Europe"){return "#A0522D";}
else if (d.name === "Europe, Central"){return "#a37c27";}
else if (d.name === "German Federal Republic"){return "#a37c27";}
else if (d.name === "Europe, Eastern"){return "#a37c27";}
else if (d.name === "Czech Republic"){return "#a37c27";}
else if (d.name === "Poland"){return "#a37c27";}
else if (d.name === "Russia"){return "#a37c27";}
else if (d.name === "Turkey"){return "#a37c27";}
else if (d.name === "Europe, Southern"){return "#a37c27";}
else if (d.name === "Italy"){return "#a37c27";}
else if (d.name === "Portugal"){return "#a37c27";}
else if (d.name === "Spain"){return "#a37c27";}
else if (d.name === "Europe, Western"){return "#a37c27";}
else if (d.name === "Belgium"){return "#a37c27";}
else if (d.name === "France"){return "#a37c27";}
else if (d.name === "Ireland"){return "#a37c27";}
else if (d.name === "Netherlands"){return "#a37c27";}
else if (d.name === "Switzerland"){return "#a37c27";}
else if (d.name === "United Kingdom"){return "#a37c27";}
else if (d.name === "Scandinavia"){return "#a37c27";}
else if (d.name === "Denmark"){return "#a37c27";}
else if (d.name === "Finland"){return "#a37c27";}
else if (d.name === "Norway"){return "#a37c27";}
else if (d.name === "Sweden"){return "#a37c27";}
else if (d.name === "North America"){return "#A0522D";}
else if (d.name === "Canada"){return "#a37c27";}
else if (d.name === "British Columbia"){return "#a37c27";}
else if (d.name === "Ontario"){return "#a37c27";}
else if (d.name === "Quebec"){return "#a37c27";}
else if (d.name === "Mexico"){return "#a37c27";}
else if (d.name === "United States"){return "#A0522D";}
else if (d.name === "Middle Atlantic States"){return "#A0522D";}
else if (d.name === "District Of Columbia"){return "#a37c27";}
else if (d.name === "Maryland"){return "#a37c27";}
else if (d.name === "Midwestern States"){return "#a37c27";}
else if (d.name === "Michigan"){return "#a37c27";}
else if (d.name === "Missouri"){return "#a37c27";}
else if (d.name === "Northeastern States"){return "#a37c27";}
else if (d.name === "Massachusetts"){return "#a37c27";}
else if (d.name === "New York"){return "#a37c27";}
else if (d.name === "Southeastern States"){return "#a37c27";}
else if (d.name === "North Carolina"){return "#a37c27";}
else if (d.name === "Southwestern States"){return "#a37c27";}
else if (d.name === "Texas"){return "#a37c27";}
else if (d.name === "Western States"){return "#a37c27";}
else if (d.name === "California"){return "#a37c27";}
else if (d.name === "Washington"){return "#a37c27";}
else if (d.name === "Pacific Ocean islands"){return "#a37c27";}
else if (d.name === "Philippines"){return "#a37c27";}
else if (d.name === "South America"){return "#A0522D";}
else if (d.name === "Argentina"){return "#a37c27";}
else if (d.name === "Brazil"){return "#a37c27";}
else if (d.name === "Chile"){return "#a37c27";}
else if (d.name === "Geopolitical Designation"){return "#4169e1";}
else if (d.name === "Codex Alimentarius Commission Countries"){return "#00bfff";}
else if (d.name === "Organization for Economic Cooperation and Development (OECD)"){return "#00bfff";}
else if (d.name === "European Union"){return "#00bfff";}
else if (d.name === "@Organization"){return "#006400";}
else if (d.name === "Consortium"){return "#006400";}
else if (d.name === "Corporation"){return "#ff0000";}
else if (d.name === "EducationalOrganization"){return "#006400";}
else if (d.name === "Government"){return "#006400";}
else if (d.name === "MedicalOrganization"){return "#006400";}
else if (d.name === "NGO"){return "#006400";}
else if (d.name === "Alianza de Servicios de Información"){return "#00ff7f";}
else if (d.name === "DBpedia"){return "#00ff7f";}
else if (d.name === "International Rice Research Institute"){return "#00ff7f";}
else if (d.name === "Wikimedia"){return "#00ff7f";}
else if (d.name === "American Food Data Systems Institute"){return "#db7093";}
else if (d.name === "Daily Care"){return "#db7093";}
else if (d.name === "Daly Food"){return "#db7093";}
else if (d.name === "Electronic Label Inc."){return "#db7093";}
else if (d.name === "Export Import Data"){return "#db7093";}
else if (d.name === "Ontomatica"){return "#db7093";}
else if (d.name === "Chinese Academy of Agricultural Science"){return "#00ff7f";}
else if (d.name === "Massachusetts Institute of Technology, CSAIL"){return "#00ff7f";}
else if (d.name === "University of Hertfordshire"){return "#00ff7f";}
else if (d.name === "University of Michigan, Ontobee"){return "#00ff7f";}
else if (d.name === "University of Sydney"){return "#00ff7f";}
else if (d.name === "European Chemicals Agency"){return "#00ff7f";}
else if (d.name === "European Food Safety Authority"){return "#00ff7f";}
else if (d.name === "US Department of Agriculture"){return "#00ff7f";}
else if (d.name === "US Food and Drug Administration"){return "#00ff7f";}
else if (d.name === "US Library of Congress"){return "#00ff7f";}
else if (d.name === "US National Institutes of Health"){return "#00ff7f";}
else if (d.name === "European Molecular Biology Laboratory"){return "#00ff7f";}
else if (d.name === "Kyoto Encyclopedia of Genes and Genomes"){return "#00ff7f";}
else if (d.name === "National Center for Biomedical Ontologies"){return "#00ff7f";}
else if (d.name === "UN Food and Agriculture Organization"){return "#00ff7f";}
else if (d.name === "@Person"){return "#48d1cc";}
else if (d.name === "Advisers"){return "#0000ff";}
else if (d.name === "Development Partners"){return "#0000ff";}
else if (d.name === "Team"){return "#0000ff";}
else if (d.name === "@CreativeWork"){return "#0000ff";}
else if (d.name === "Dataset"){return "#d6618f";}
else if (d.name === "Data Feed"){return "#f3d480";}
else if (d.name === "Data Feed - Supplier Data"){return "#f1931b";}
else if (d.name === "Data Feed - Ontology"){return "#8f715b";}
else if (d.name === "Data Feed - Knowledge Graph Kit"){return "#36688d";}
else if (d.name === "Diet"){return "#a7414a";}
else if (d.name === "HowTo"){return "#423a01";}
else if (d.name === "Recipe"){return "#776b04";}
else if (d.name === "Learning Resource"){return "#003d73";}
else if (d.name === "Course"){return "#0878a4";}
else if (d.name === "Menu"){return "#a7414a";}
else if (d.name === "Software Application"){return "#582a20";}
else if (d.name === "@Medical Entity"){return "#0000ff";}
else if (d.name === "Anatomical Structure"){return "#0878a4";}
else if (d.name === "Bone"){return "#1ecfd6";}
else if (d.name === "Brain Structure"){return "#1ecfd6";}
else if (d.name === "Joint"){return "#1ecfd6";}
else if (d.name === "Ligament"){return "#1ecfd6";}
else if (d.name === "Muscle"){return "#1ecfd6";}
else if (d.name === "Nerve"){return "#1ecfd6";}
else if (d.name === "Vessel"){return "#1ecfd6";}
else if (d.name === "Artery"){return "#edd179";}
else if (d.name === "Lymphatic Vessel"){return "#edd179";}
else if (d.name === "Vein"){return "#edd179";}
else if (d.name === "Anatomical System"){return "#0878a4";}
else if (d.name === "Lifestyle Modification"){return "#0878a4";}
else if (d.name === "Medical Intangible"){return "#0878a4";}
else if (d.name === "Dose Schedule"){return "#1ecfd6";}
else if (d.name === "Maximum DoseSchedule"){return "#edd179";}
else if (d.name === "Recommended DoseSchedule"){return "#edd179";}
else if (d.name === "Reported DoseSchedule"){return "#edd179";}
else if (d.name === "Drug Legal Status"){return "#1ecfd6";}
else if (d.name === "Drug Strength"){return "#1ecfd6";}
else if (d.name === "Medical Code"){return "#1ecfd6";}
else if (d.name === "Medical Risk Estimator"){return "#0878a4";}
else if (d.name === "Medical RiskCalculator"){return "#1ecfd6";}
else if (d.name === "Medical Study"){return "#0878a4";}
else if (d.name === "Medical ObservationalStudy"){return "#1ecfd6";}
else if (d.name === "Substance"){return "#0878a4";}
else if (d.name === "Dietary Supplement"){return "#1ecfd6";}
else if (d.name === "Drug"){return "#1ecfd6";}

else {return "#FFFFFF";}
}
)

// LINKS
.linkWidth(2)
.linkOpacity(0.5)
.linkThreeObjectExtend(true)

.linkThreeObject(link => {
// const sprite = new SpriteText(`${link.source} \u2194 ${link.target}`);
const sprite = new SpriteText(`${link.label}`);
sprite.color = "#D3D3D3"; // beige-tan
sprite.textHeight = 3.5;
return sprite;
}
)

.linkPositionUpdate((sprite, { start, end }) => {
const middlePos = Object.assign(...["x", "y", "z"].map(c => ({
[c]: start[c] + (end[c] - start[c]) / 2
}
))
);
Object.assign(sprite.position, middlePos);
}
)

.linkDirectionalParticles("value")
.linkDirectionalParticleSpeed(d => d.value * 0.001)

<!-- LINK color may need to use IDN; unless: add 'target' to declarations -->
<!-- better approach: target predicates -->

.linkColor(d => {
     if (d.type === "inLanguage"){return "#32CD32";}
else if (d.type === "priority"){return "#FF0000";}
<!-- else if (d.target === ""){return "#2E8BC0";} -->
<!-- else if (d.target === ""){return "#2E8BC0";} -->
<!-- else if (d.target === ""){return "#2E8BC0";} -->
<!-- else if (d.target === ""){return "#2E8BC0";} -->
<!-- else if (d.target === ""){return "#2E8BC0";} -->
<!-- else if (d.target === ""){return "#2E8BC0";} -->

else {return "#FCFF98";} // yellow, green; light

})

.onNodeDragEnd(node => {
node.fx = node.x;
node.fy = node.y;
node.fz = node.z;
}
);

Graph.d3Force("error")
.strength(-60);

</script>
