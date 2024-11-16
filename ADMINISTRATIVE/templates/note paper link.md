<%*
const referenceFolder = 'References'; // Folder where reference notes are stored

// Get the entire content of the current note
const noteContent = tp.file.content;

// Match the last heading in the note, assuming the paper title is a heading
const headings = noteContent.match(/^#\s+(.+)/gm); // This matches all headings starting with '# '
let paperTitle = headings ? headings[headings.length - 1].replace(/^#\s+/, '').trim() : null;

if (paperTitle) {
   // Format the paper title to create a valid file name (adjust to your naming convention)
   const formattedTitle = paperTitle.replace(/[^a-zA-Z0-9 ]/g, '').trim();

   // Create a relative link to the reference note based on the paper title
   const linkToNote = `[[${referenceFolder}/${formattedTitle}]]`;

   // Insert the link into the current note
   tR += linkToNote;
} else {
   tR += 'No paper title found at the bottom of the note.';
}
%>
