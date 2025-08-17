+++
title = "Pharos"
[data]
baseChartOn = 3
colors = ["#627c62", "#11819b", "#ef7f1a", "#4e1154"]
columnTitles = ["Section", "Status", "Author"]
fileLink = "content/projects.csv"
title = "Projects"
+++

{{< block "grid-2" >}}
{{< column >}}

# Track and Act on threats.

Pharos allows to take control on threats on your systems.

{{< tip >}}
Pick existing plugins or write your own using [starlark](https://github.com/metraction/pharos-plugins/blob/main/image-exemptions/exemption.star) ir [go templates](https://github.com/metraction/pharos-plugins/blob/main/owner/owners_v1.hbs)
{{< /tip >}}


{{< tip >}}
Modify plugin data in your git repo 
![plugin-data](/images/home/1-modify-plugin.png)
{{< /tip >}}

{{< tip >}}
Create configmap out of [plugin data](https://github.com/metraction/pharos/blob/main/testdata/enrichers-git/enrichers.yaml)
```bash
pharos plugin configmap enrichers.yaml > configmap-enrichers.yaml
```
{{< /tip >}}

{{< tip >}}
Apply that configmap to your cluster
```bash
kubectl apply -f helm/pharos/templates/configmap-enrichers.yaml
``` 
{{< /tip >}}

{{< button "docs/" "Read the Docs" >}}
{{< /column >}}

{{< column >}}
<img src="/images/vente-small.png" alt="diy" style="display:block;margin:0 auto;max-width:100%;height:auto;" />
{{< /column >}}
{{< /block >}}
