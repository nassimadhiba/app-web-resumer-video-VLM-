Résumé Vidéo Automatique avec API Flask + Intégration Laravel

Ce projet permet de résumer automatiquement une vidéo en combinant transcription audio, analyse visuelle et génération de résumé textuel, puis en créant une vidéo résumée avec narration audio. Il inclut également une application Laravel pour consommer cette API.

Fonctionnalités principales
1. Traitement vidéo avec Flask

Extraction des frames : Capture des images clés de la vidéo.

Génération de légendes (captions) : Utilise BLIP pour décrire chaque frame.

Transcription audio : Utilise Whisper pour convertir la piste audio en texte.

Résumé du contenu : Combine les légendes et la transcription pour générer un résumé via BART.

Création de la vidéo résumée : Synchronisation des frames avec l’audio généré via gTTS.

API Flask : Route /upload_video pour uploader une vidéo et recevoir la vidéo résumée.

Exposition publique : Utilisation de ngrok pour accéder à l’API depuis Internet.

2. Application Laravel

Frontend pour uploader la vidéo depuis un navigateur.

Consommation de l’API Flask via HTTP POST (/upload_video).

Affichage du lien ou téléchargement de la vidéo résumée.

Optionnel : Historique des vidéos uploadées et résumées.

Dépendances
Flask / Python

flask, flask-ngrok, pyngrok

torch, transformers (BLIP et BART)

whisper

opencv-python, Pillow

moviepy, gTTS

Laravel / PHP

Laravel 10+

GuzzleHttp pour les requêtes API

Frontend Blade / Bootstrap pour l’upload et affichage des vidéos

Pipeline de traitement

Upload vidéo depuis Laravel → API Flask (/upload_video).

Extraction des frames par Flask.

Génération des captions pour chaque frame.

Transcription audio.

Résumé textuel combinant captions + transcription.

Création vidéo résumée avec narration.

Retour du fichier vidéo à Laravel pour téléchargement ou lecture.
