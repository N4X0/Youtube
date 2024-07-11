import yt_dlp
from moviepy.editor import VideoFileClip

# Function to download the video from YouTube
def download_video(url, output_path='video.mp4'):
    ydl_opts = {
        'format': 'best',
        'outtmpl': output_path,
    }
    with yt_dlp.YoutubeDL(ydl_opts) as ydl:
        ydl.download([url])
    print(f'Downloaded: {output_path}')
    return output_path

# Function to convert MP4 to MP3
def convert_mp4_to_mp3(input_path, output_path='audio.mp3'):
    video = VideoFileClip(input_path)
    audio = video.audio
    audio.write_audiofile(output_path)
    print(f'Converted: {output_path}')

# YouTube video URL
youtube_url = 'https://www.youtube.com/watch?v=bZxOOy2_JSQ '

# Output paths for the downloaded video and audio file
video_path = 'video.mp4'
audio_path = 'audio.mp3'

# Download the YouTube video
downloaded_video_path = download_video(youtube_url, video_path)

# Convert the downloaded video to MP3
convert_mp4_to_mp3(downloaded_video_path, audio_path)
