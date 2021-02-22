# origo-export-etuna

Knapp som skickar anrop till Eskilstunas .NET projekt för fastighetsrapporter.

**Parametrar:**
- layer: Lagernamnet för fastigheter
- hostname: URL till önskad host som kör tjänsten för .NET projektet. Ta inte med backslash i slutet av URL:en.
- attribute: Det attribut för id/fnr som ska skickas med i anropet.
- buttonText: Knappens text.

**Exempel:**
```HTML
<script type="text/javascript">
    var origo = Origo('index.json');
    origo.on('load', function (viewer) {
      var origoexportetuna = Origoexportetuna({
        layer: "sokvyx_djupdata_djuppunkter_vy",
        hostname: "https://ikarta.eskilstuna.se",
        attribute: "fnr",
        buttonText: "Hämta excel"
      });
      viewer.addComponent(origoexportetuna);
    });
</script>
```

### Knappens placering med origo-servers excelcreator
![](hamtaexcel1.gif)

### Knappens placering utan origo-servers excelcreator
![](hamtaexcel2.gif)
