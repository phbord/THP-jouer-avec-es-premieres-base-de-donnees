# Requêtes SQL des infos demandées sur notre BDD musicale

## Récupérer tous les albums
`SELECT * FROM albums;`

## Récupérer tous les albums dont le titre contient "Great"
`SELECT *FROM albums WHERE Title LIKE '%Great%';`

## Donner le nombre total d'albums contenus dans la base
`SELECT COUNT(Title) FROM  albums;`

## Supprimer tous les albums dont le nom contient "music"
`DELETE FROM albums WHERE Title LIKE '%music%';`

## Récupérer tous les albums écrits par AC/DC
`SELECT albums.Title FROM  albums INNER JOIN artists ON albums.ArtistId=artists.ArtistId AND artists.Name="AC/DC";`

## Récupérer tous les titres des albums de AC/DC
`SELECT tracks.Name, albums.Title, artists.Name FROM albums INNER JOIN artists ON albums.ArtistId=artists.ArtistId AND artists.Name="AC/DC" INNER JOIN tracks ON albums.AlbumId=tracks.AlbumId;`

## Récupérer la liste des titres de l'album "Let There Be Rock"
`SELECT tracks.Name, albums.Title, artists.Name FROM albums INNER JOIN artists ON albums.ArtistId=artists.ArtistId AND artists.Name="AC/DC" AND albums.Title="Let There Be Rock" INNER JOIN tracks ON albums.AlbumId=tracks.AlbumId;`

## Afficher le prix de cet album ainsi que sa durée totale
`SELECT SUM(tracks.UnitPrice) FROM albums INNER JOIN artists ON albums.ArtistId=artists.ArtistId AND artists.Name="AC/DC" AND albums.Title="Let There Be Rock" INNER JOIN tracks ON albums.AlbumId=tracks.AlbumId;`

## Afficher le coût de l'intégralité de la discographie de "Deep Purple"
`SELECT SUM(tracks.UnitPrice) FROM albums INNER JOIN artists ON albums.ArtistId=artists.ArtistId AND artists.Name="Deep Purple" INNER JOIN tracks ON albums.AlbumId=tracks.AlbumId;`

## Créer l'album de ton artiste favori en base
- en renseignant correctement les 3 tables
  - *albums*
  - *artists*
  - *tracks*
`SELECT tracks.Name, artists.Name FROM albums INNER JOIN artists ON albums.ArtistId=artists.ArtistId AND artists.Name="AC/DC" INNER JOIN tracks ON tracks.AlbumId=albums.AlbumId ORDER BY tracks.Name DESC LIMIT 12;`
``