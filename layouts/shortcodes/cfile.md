{{- $book := index .Site.Data.files (.Get 0)}}
{{- if $book }}
[({{- $book.filename -}} &nbsp; {{- $book.size_str -}})]({{- $book.url -}})
{{- else }}
{{ errorf "Couldn't get Canvas File (cfile) `%s`" (.Get 0) }}
{{- end }}