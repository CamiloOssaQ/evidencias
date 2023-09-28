[Inicio](./index.md)

## Sesión 8 


### Se desea crear una jerarquía de clases que permita representar diferentes tipos de música. Se ha decidido crear una superclase Musica que tenga los métodos y atributos comunes a todas las clases hijas.

```java
import java.util.ArrayList;
import java.util.List;

public abstract class Musica {
    private String titulo;

    public Musica(String titulo) {
        this.titulo = titulo;
    }

    public abstract void play();

    public abstract void stop();

    public abstract void pause();

    public abstract void next();

    public abstract void previous();
}

public class Cancion extends Musica {
    private String artista;
    private String album;

    public Cancion(String titulo, String artista, String album) {
        super(titulo);
        this.artista = artista;
        this.album = album;
    }

    @Override
    public void play() {
        System.out.println("Reproduciendo la canción: " + titulo + " - Artista: " + artista + " - Álbum: " + album);
    }

    @Override
    public void stop() {
        System.out.println("Deteniendo la reproducción de la canción: " + titulo);
    }

    @Override
    public void pause() {
        System.out.println("Pausando la reproducción de la canción: " + titulo);
    }

    @Override
    public void next() {
        System.out.println("Avanzando a la siguiente canción");
    }

    @Override
    public void previous() {
        System.out.println("Retrocediendo a la canción anterior");
    }
}

public class BandaSonora extends Musica {
    private String autor;

    public BandaSonora(String titulo, String autor) {
        super(titulo);
        this.autor = autor;
    }

    @Override
    public void play() {
        System.out.println("Reproduciendo la banda sonora: " + titulo + " - Autor: " + autor);
    }

    @Override
    public void stop() {
        System.out.println("Deteniendo la reproducción de la banda sonora: " + titulo);
    }

    @Override
    public void pause() {
        System.out.println("Pausando la reproducción de la banda sonora: " + titulo);
    }

    @Override
    public void next() {
        System.out.println("Avanzando a la siguiente pista de la banda sonora");
    }

    @Override
    public void previous() {
        System.out.println("Retrocediendo a la pista anterior de la banda sonora");
    }
}

public class Album extends Musica {
    private List<Cancion> canciones;
    private List<String> autores;

    public Album(String titulo, List<Cancion> canciones, List<String> autores) {
        super(titulo);
        this.canciones = canciones;
        this.autores = autores;
    }

    @Override
    public void play() {
        System.out.println("Reproduciendo el álbum: " + titulo);
        for (Cancion cancion : canciones) {
            cancion.play();
        }
    }

    @Override
    public void stop() {
        System.out.println("Deteniendo la reproducción del álbum: " + titulo);
        for (Cancion cancion : canciones) {
            cancion.stop();
        }
    }

    @Override
    public void pause() {
        System.out.println("Pausando la reproducción del álbum: " + titulo);
        for (Cancion cancion : canciones) {
            cancion.pause();
        }
    }

    @Override
    public void next() {
        System.out.println("Avanzando a la siguiente canción del álbum");

    @Override
    public void previous() {
        System.out.println("Retrocediendo a la canción anterior del álbum");

    }
}

public class Main {
    public static void main(String[] args) {
        Cancion intro = new Cancion("Intro", "Metricas Frias", "Despues de muertos");
        Cancion horaPico = new Cancion("Hora pico", "COQE", "Despues de muertos");
        Cancion miComedia = new Cancion("Mi comedia", "Doble Porcion", "Despues de muertos");
        Cancion ultimaLlamada = new Cancion("Ultima llamada", "Metricas Frias", "Despues de muertos");
        Cancion ole = new Cancion("Ole", "COQE", "Despues de muertos");
        Cancion vidaEsBonita = new Cancion("La vida es bonita", "Doble Porcion", "Despues de muertos");
        Cancion finDelMundo = new Cancion("El fin del mundo", "Metricas Frias", "Despues de muertos");
        Cancion colorLila = new Cancion("Color lila", "COQE", "Despues de muertos");
        Cancion atico = new Cancion("El atico(Outro)", "Doble Porcion", "Despues de muertos");

        Cancion tierra = new Cancion("T.ierra", "Mañas Rufino", "Tamara");
        Cancion amor = new Cancion("A.mor", "Mañas Rufino", "Tamara");
        Cancion musica = new Cancion("M.usica", "Mañas Rufino", "Tamara");
        Cancion agua = new Cancion("A.gua", "Mañas Rufino", "Tamara");
        Cancion raices = new Cancion("R.aices", "Mañas Rufino", "Tamara");
        Cancion aire = new Cancion("A.ire", "Mañas Rufino", "Tamara");

        Cancion starWars = new Cancion("Star Wars", "John Williams", "Star Wars");
        Cancion rebelFanfare = new Cancion("Rebel Fanfare", "John Williams", "Star Wars");

        List<Cancion> cancionesDespuesDeMuertos = new ArrayList<>();
        cancionesDespuesDeMuertos.add(intro);
        cancionesDespuesDeMuertos.add(horaPico);
        cancionesDespuesDeMuertos.add(miComedia);
        cancionesDespuesDeMuertos.add(ultimaLlamada);
        cancionesDespuesDeMuertos.add(ole);
        cancionesDespuesDeMuertos.add(vidaEsBonita);
        cancionesDespuesDeMuertos.add(finDelMundo);
        cancionesDespuesDeMuertos.add(colorLila);
        cancionesDespuesDeMuertos.add(atico);

        List<String> autoresDespuesDeMuertos = new ArrayList<>();
        autoresDespuesDeMuertos.add("Metricas Frias");
        autoresDespuesDeMuertos.add("COQE");
        autoresDespuesDeMuertos.add("Doble Porcion");

        List<Cancion> cancionesTamara = new ArrayList<>();
        cancionesTamara.add(tierra);
        cancionesTamara.add(amor);
        cancionesTamara.add(musica);
        cancionesTamara.add(agua);
        cancionesTamara.add(raices);
        cancionesTamara.add(aire);

        List<String> autoresTamara = new ArrayList<>();
        autoresTamara.add("Mañas Rufino");
        autoresTamara.add("Doble Porcion");

        List<Cancion> cancionesStarWars = new ArrayList<>();
        cancionesStarWars.add(starWars);
        cancionesStarWars.add(rebelFanfare);

        List<String> autoresStarWars = new ArrayList<>();
        autoresStarWars.add("John Williams");

        Album despuesDeMuertos = new Album("Despues de muertos", cancionesDespuesDeMuertos, autoresDespuesDeMuertos);
        Album tamara = new Album("Tamara", cancionesTamara, autoresTamara);
        BandaSonora starWarsBandaSonora = new BandaSonora("Star Wars", "John Williams", cancionesStarWars, autoresStarWars);

        despuesDeMuertos.play();
        tamara.play();
        starWarsBandaSonora.play();
    }
}

```