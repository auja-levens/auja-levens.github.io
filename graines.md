## Test de publication

### Gestions des graines

<hr>

#### 1. Injection via javascript

<table id="stock">
  <thead>
    <tr>
     <th>Variété</th>
     <th>Quantité</th>
    </tr>
  </thead>

  <tbody>
  </tbody>
</table>

<script>
//(function(){})();

var url = 'https://docs.google.com/spreadsheets/d/e/2PACX-1vRnjpwv9eYPwZx__7-8H4EYoe7Zs4yXZwCAuPJuxNEfj3LgInGX6-e-94SI7BPI7FF7YrVqP3NYO3bN/pub?gid=1185466709&single=true&output=tsv';
var stock = document.getElementById('stock');

var opts = {
    method: 'GET',
    headers: {}
};

fetch(url, opts).then(function (response) {
    return response.text();
})
    .then(function (text) {
        var lines = text.split("\n")
        var i, l, cols, row, cell0, cell1;
        for(i = lines.length-1; i > 1; i--) { // skip bogus headers in tsv (0, 1)
            l = lines[i];
            cols = l.split('\t')
            row = stock.insertRow(1); // skip table header

            cell0 = row.insertCell(0)
            cell0.innerHTML = cols[0];

            cell1 = row.insertCell(1)
            cell1.innerHTML = cols[1];
            cell1.style.textAlign = "right"
        }

    });
</script>

<hr>

#### 2. Liens externes

- [lien externe (html)](https://docs.google.com/spreadsheets/d/e/2PACX-1vRnjpwv9eYPwZx__7-8H4EYoe7Zs4yXZwCAuPJuxNEfj3LgInGX6-e-94SI7BPI7FF7YrVqP3NYO3bN/pubhtml?gid=1185466709&single=true)
- [lien externe (tsv)](https://docs.google.com/spreadsheets/d/e/2PACX-1vRnjpwv9eYPwZx__7-8H4EYoe7Zs4yXZwCAuPJuxNEfj3LgInGX6-e-94SI7BPI7FF7YrVqP3NYO3bN/pub?gid=1185466709&single=true&output=tsv)
- [lien externe (csv)](https://docs.google.com/spreadsheets/d/e/2PACX-1vRnjpwv9eYPwZx__7-8H4EYoe7Zs4yXZwCAuPJuxNEfj3LgInGX6-e-94SI7BPI7FF7YrVqP3NYO3bN/pub?gid=1185466709&single=true&output=csv)

<hr>

#### 3. Iframe

<iframe width="100%" height="300px" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRnjpwv9eYPwZx__7-8H4EYoe7Zs4yXZwCAuPJuxNEfj3LgInGX6-e-94SI7BPI7FF7YrVqP3NYO3bN/pubhtml?gid=1185466709&amp;single=true&amp;widget=true&amp;headers=false"></iframe>

<hr>

## Welcome to GitHub Pages2

You can use the [editor on GitHub](https://github.com/auja-levens/auja-levens.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/auja-levens/auja-levens.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
