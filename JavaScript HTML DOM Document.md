>Lista para usar o objeto document (DOM), podendo acessar e manipular HTML

Site com exemplos práticos: https://javascript.info/dom-attributes-and-properties

---
### Encontrando Elementos HTML:
>Por [[Class e Id]] e [[Tags HTML]]

|Method|Description|
|---|---|
|document.getElementById(_id_)|Find an element by element id|
|document.getElementsByTagName(_name_)|Find elements by tag name|
|document.getElementsByClassName(_name_)|Find elements by class name|

---

### Alterando Elementos HTML
>Como adicionar novas tags HTML; valores a elementos; estilizar elementos e a adicionar atributos com um valor.

|Property|Description|
|---|---|
|_element_.innerHTML =  _new html content_|Change the inner HTML of an element|
|_element_._attribute = new value_|Change the attribute value of an HTML element|
|_element_.style._property = new style_|Change the style of an HTML element|
|Method|Description|
|_element_.setAttribute_(attribute, value)_|Change the attribute value of an HTML element|

---

### Adicionando e excluindo elementos
1. Como criar elementos no HTML.
2. Remover elementos do HTML.
3. Adicionar um elemento no HTML.
4. Substituir um elemento antigo pelo novo, sendo o primeiro parâmetro o que irá ser adicionado e o segundo o que será removido.
5. Escreva no fluxo de saída HTML - **Não sei o que significa**

|Method|Description|
|---|---|
|document.createElement(_element_)|Create an HTML element|
|document.removeChild(_element_)|Remove an HTML element|
|document.appendChild(_element_)|Add an HTML element|
|document.replaceChild(_new, old_)|Replace an HTML element|
|document.write(_text_)|Write into the HTML output stream|
### Encontrando objetos HTML:

>O primeiro HTML DOM Nível 1 (1998), definiu 11 objetos HTML, coleções de objetos e propriedades. Eles ainda são válidos em HTML5. Mais tarde, no HTML DOM Nível 3, mais objetos, coleções e propriedades foram adicionados.

| Property | Description | DOM |
| ---- | ---- | ---- |
| document.anchors | Returns all <a> elements that have a name attribute | 1 |
| document.applets | Deprecated | 1 |
| document.baseURI | Returns the absolute base URI of the document | 3 |
| document.body | Returns the <body> element | 1 |
| document.cookie | Returns the document's cookie | 1 |
| document.doctype | Returns the document's doctype | 3 |
| document.documentElement | Returns the <html> element | 3 |
| document.documentMode | Returns the mode used by the browser | 3 |
| document.documentURI | Returns the URI of the document | 3 |
| document.domain | Returns the domain name of the document server | 1 |
| document.domConfig | Obsolete. | 3 |
| document.embeds | Returns all <embed> elements | 3 |
| document.forms | Returns all <form> elements | 1 |
| document.head | Returns the <head> element | 3 |
| document.images | Returns all <img> elements | 1 |
| document.implementation | Returns the DOM implementation | 3 |
| document.inputEncoding | Returns the document's encoding (character set) | 3 |
| document.lastModified | Returns the date and time the document was updated | 3 |
| document.links | Returns all <area> and <a> elements that have a href attribute | 1 |
| document.readyState | Returns the (loading) status of the document | 3 |
| document.referrer | Returns the URI of the referrer (the linking document) | 1 |
|document.strictErrorChecking|Returns if error checking is enforced|3|
|document.title|Returns the title element|1|
|document.URL|Returns the complete URL of the document|1|
|document.scripts|Returns all script elements|  |


---
Fontes:
- https://www.w3schools.com/js/js_htmldom_document.asp

Tags: #softwaredevelopment 