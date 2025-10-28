**Résumé Vidéo Automatique**
Description

Ce projet permet de résumer automatiquement une vidéo en combinant transcription audio, analyse visuelle et génération de résumé textuel, puis en créant une vidéo résumée avec narration audio.

Le projet peut être utilisé facilement via une API Flask et exposé publiquement pour des tests ou pour une intégration web grâce à ngrok.

**Fonctionnalités**

Extraction des frames : Capture d’images à intervalles réguliers pour représenter le contenu visuel de la vidéo.

Génération de légendes : Utilisation de BLIP (Salesforce/blip-image-captioning-base) pour générer des descriptions textuelles pour chaque image.

Transcription audio : Whisper convertit automatiquement l’audio de la vidéo en texte.

Résumé textuel : BART (facebook/bart-large-cnn) crée un résumé combinant transcription audio et légendes visuelles.

Vidéo résumée avec audio narratif : gTTS transforme le résumé en audio, synchronisé avec les images via MoviePy.

API Flask : Route /upload_video pour uploader une vidéo et obtenir le résumé.

Exposition publique : Ngrok rend l’API accessible sur Internet pour tests ou intégration web.

**Technologies et Outils**

Langages : Python

Frameworks et API :

Flask → Création de l’API

Flask-Ngrok / Pyngrok → Exposition publique de l’API

Deep Learning & NLP :

Torch / Transformers → BLIP et BART pour analyse visuelle et résumé

Whisper → Transcription audio

Traitement vidéo et audio :

OpenCV / Pillow → Extraction et traitement des frames

MoviePy → Montage vidéo et synchronisation audio

gTTS → Conversion du texte en narration audio

**Environnement & Déploiement** :

Google Colab / VS Code → Développement et tests
