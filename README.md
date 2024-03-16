interface MediaPlayer{
    public void play();
    public void pause();
    public void stop();
}
interface AdvancedMediaPlayer extends MediaPlayer{
    public void adjustVolume();
    public void SkipTrack();
}
interface PlaylistMediaPlayer extends AdvancedMediaPlayer{
    public void ManagePlaylist();
}
class VLCMediaPlayer implements PlaylistMediaPlayer{
    @Override
    public void play(){
        System.out.println("you can play");
    }
    @Override
    public void pause(){
        System.out.println("you can pause");
    }
    @Override
    public void stop(){
        System.out.println("you can stop");
    }
    @Override
    public void adjustVolume(){
        System.out.println("Volume can be changed");
    }
    @Override
    public void SkipTrack(){
        System.out.println("you can skip the track");
    }
    @Override
    public void ManagePlaylist(){
        System.out.println("you can create play list");
        System.out.println("you can add media items to playlist");
    }
}

public class VCPlayer
{
    public static void main(String[] args)
    {
      VLCMediaPlayer  player = new VLCMediaPlayer();
      player.play();
      player.pause();
      player.stop();
      player.adjustVolume();
      player.SkipTrack();
      player.ManagePlaylist();
    }
}
