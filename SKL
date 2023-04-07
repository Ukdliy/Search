function doGet() {
  var template = HtmlService.createTemplateFromFile('Page');
  return template.evaluate();
}

function searchNPSN(npsn) {
  var sheet = SpreadsheetApp.getActiveSpreadsheet().getSheetByName("SKL"); // Ganti Sheet1 dengan nama sheet Anda
  var data = sheet.getDataRange().getValues();
  var result = [];

  for (var i = 1; i < data.length; i++) { // Mulai dari baris kedua karena baris pertama adalah header
    if (data[i][1] == npsn) { // Kolom NPSN berada di indeks 1
      result.push(data[i]);
    }
  }

  if (result.length > 0) {
    return result;
  } else {
    return "Data Tidak Ditemukan";
  }
}
