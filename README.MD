# Git History and File Structure Data Visualization, a bibliography

Some great resources for data visualization:

### Gource

#### What does it do?
Generates mp4 videos of a project's source control history

Read more about it here:
https://github.com/acaudwell/Gource/wiki/Controls

#### Setting it up
Gource requires FFMPEG to run

```
brew install ffmpeg
```

install Gource
```
brew install gource
```

CD into the root directory of your favorite project, type the following command and let 'er rip!

```
gource
```

For more customization check out the above wiki, here's a helpful more advanced command, hide directory and filenames in the video, also output the video to your very own MP4.
 
```
gource --hide dirnames,filenames --seconds-per-day 0.1 --auto-skip-seconds 1 -1280x720 -o - | ffmpeg -y -r 60 -f image2pipe -vcodec ppm -i - -vcodec libx264 -preset ultrafast -pix_fmt yuv420p -crf 1 -threads 0 -bf 0 gource.mp4
```

## CodeFlowers

A gorgeous open source visualization project that shows the file structure and its dependencies and relationships. Each orb represents a file in your project, the size of each node is reflective of the number lines of code within the file.

#### Setting it up
This graph is ingests JSON data that represents a file tree. Each node of the tree represents a file, the file object contains the following attributes: `name`, `language`, `size`, where `size` is the number of lines in the file. The CLOC library is a great resource for counting the lines of code within your projects.

Check out the CLOC documentation for more information
http://cloc.sourceforge.net/ 

Read more about it here:
https://github.com/fzaninotto/CodeFlower

## D3.js

A fantastic library for all your data visualization needs!
https://github.com/d3/d3


