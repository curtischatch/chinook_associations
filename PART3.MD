Find the album titled "Vinicius De Moraes", and then use an association-provided method to find all its tracks.

  a = Album.where(title: "Vinicius De Moraes")
  a.first.track.pluck(:name)

Find the artist called "Philip Glass Ensemble", and then use an association-provided method to find all their albums.

  a = Album.where(name: "Philip Glass Ensemble")
  a.first.albums.pluck(:title)


Find the "Brazilian Music" playlist and then use an association-provided method to find all its tracks.

  a = Playlist.where(name: "Brazilian Music")
  a =first.tracks.all


Find the "Jazz" genre and then use an association-provided method to find all its tracks.

  a = Genre.where(name: "Jazz")
  a.first.tracks.pluck(:name)

Find the track "My Time After Awhile" and then use an association-provided method to find its genre.

  a = Track.where(name: "My Time After Awhile")
  a.first.genre.name

Use an association-provided method to find the media type of that same track.

  a.first.media_type


Use an association-provided method to find the album that track appears on.

  a.first.album
