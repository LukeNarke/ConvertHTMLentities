# ConvertHTMLentities

function convertHTML(str) {
  const entities = {
    "&": "&amp;",
    "<": "&lt;",
    ">": "&gt;",
    "\"": "&quot;",
    "'": "&apos;",
  };

  let arr = str.split("").map(function (elem) {
    if (entities.hasOwnProperty(elem)) {
      return entities[elem];
    } else {
      return elem;
    }
  })
  return arr.join("");
}
