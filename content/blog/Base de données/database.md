---
title: "Base de données"
date: "2020"
---

Voici un tableau affichant les données à partir du fichier CSV.

{{ $csv := test.csv.project.Test }}
<table>
  <thead>
    <tr>
      {{ range first 1 $csv }}
        {{ range . }}
          <th>{{ . }}</th>
        {{ end }}
    </tr>
  </thead>
  <tbody>
    {{ range after 1 $csv }}
      <tr>
        {{ range . }}
          <td>{{ . }}</td>
        {{ end }}
      </tr>
    {{ end }}
  </tbody>
</table>