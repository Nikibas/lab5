**Васильев Никита 803в2.**  
В проект добавил activity. На него поместил VideoView:  
![image info](/imgs/moblab2.png)  
В папку ресурсов загрузил видео  
![image info](/imgs/moblab3.png)   
В MainActivity.java инициализируем MediaController для добавления элементов управления и пропишем путь к файлу для VideoView:  
```Java
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        VideoView videoView =(VideoView)findViewById(R.id.videoView);
        MediaController mediaController= new MediaController(this);
        mediaController.setAnchorView(videoView);
        Uri uri = Uri.parse("android.resource://" + getPackageName() + "/" + R.raw.videomob);
        videoView.setMediaController(mediaController);
        videoView.setVideoURI(uri);
        videoView.requestFocus(); 
        videoView.start();
    }
```  
Запуск приложения на устройстве:  
![image info](/imgs/mob1.jpeg)  
