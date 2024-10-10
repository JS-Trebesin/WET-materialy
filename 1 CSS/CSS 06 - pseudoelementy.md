# Pseudoelementy v CSS

Pseudoelementy jsou speciální selektory v CSS, které umožňují stylovat určité části elementu nebo vkládat obsah před nebo za element. Pseudoelementy zapisujeme s dvojitou dvojtečkou `::before`. Zde jsou nejdůležitější pseudoelementy:

## ::before a ::after

Tyto pseudoelementy umožňují vložit obsah před nebo za vybraný element.

```css
.ukazka::before {
    content: "Před ";
    color: red;
}

.ukazka::after {
    content: " Po";
    color: blue;
}
```
