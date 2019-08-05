# es6-download-pdf-base64
/**
 * Creates an anchor element `<a></a>` with
 * the base64 pdf source and a filename with the
 * HTML5 `download` attribute then clicks on it.
 * @param  {string} pdf
 * @return {void}
 */
const downloadPDF = pdf => {
  const source = `data:application/pdf;base64,${pdf}`;
  const link = document.createElement('a');
  const file = 'file.pdf';

  link.href = source;
  link.download = file;
  link.click();
};
