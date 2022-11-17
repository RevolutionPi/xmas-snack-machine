# QR-Code Generation
set the in the node "--->SET WORK DIR<---" your working directory
all generated QR-Codes will be stored to this path into "codes" directory

# QR-Code PDF Generation
Maintain the source CSV filepath to read from "--->READ CSV-FILE PATH<---"
Maintain the destination filepath where a html file can be written "--->WRITE HTML-FILE PATH<---"
Open the HTML and save it to PDF or print it directly from your browser

# QR-Code Scan
The flow is preconfigured to read from a RS232 Scanner device wich is sending binary buffers with CRLF suffix
The scanned code will be published to the local mqtt broker

# Thin-Edge Integration
tbd
