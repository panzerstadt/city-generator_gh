Design Augmentation Tool pre-alpha 0.1

The question of the relevance of the creative design process (as we are taught in school) in the contemporary world has always been a question I could not find an answer for.

The current world as we are living in it is now more interconnected than ever, more full of measurable data that is possible to comprehend.
With it, the expectations of design architects to handle more and more data are making it increasingly difficult for architects themselves to find time to think creatively about their design, as we are often too bogged down by the torrent of requirements and regulations and sustainability goals.
It takes an extensive amount of mental fortitude to wade through all the legwork to get at the opportunity to do what all architects are thought to do in school, which is designing.
Either that, or a lot of people. I mean, I can't afford to pay a lot of people to do legwork for me, so that's not an option.

Even so, the human mind is only capable of juggling a limited (and actually quite small) amount of data at the same time. 
It is difficult to contemplate a complete model of a site context, much less all the deeper, unexplored nuances of soil composition, wireless data, twitter feeds, viewsheds, rainwater flow through the site, all at the same time. 
It is difficult to come up with novel, elegant, or playful yet complete solutions to a question that spans many fields of study.

We need the ability to perform data chunking in the mind, of the compression of data into useful black boxes that we can then piece together to find novel connections (read: creative leaps).
Having more data ready to be visualised and held up to the scrutiny of the mind allows the mind a broader field of ideas in which to make connections.
Thus, having more data that is easily malleable (so that it can be understood in whatever form the mind fancies) allows the designer, crucially, to have more time, hence opportunities to think about design.

Barbara Oakley describes in her talk on learning how to learn at Google: https://www.youtube.com/watch?v=vd2dtkMINIw

This tool aims at lightening that mental load by putting everything at the designer's fingertips (and mostly real-time), 
allowing him/her to see from a bird's eye view things that are relevant/interest him on the site - 
be they visible like topography, surrounding buildings, trees; 
to invisible, like wind, twitter feeds, optimal routes to and from site; 
to temporal, like patterns of weather over time, traffic data.

It is meant to be the beginnings of a lego set that makes all real world data equally accessible on the grasshopper canvas, 
enabling the capable designer to freely manipulate things like live weather data, or historical patterns in erosion, or soil type in the same way they manipulate a point of a surface in 3d space.
Do what you want with it, mix datasets together and see what happens, make designs that react to their immediate surroundings based on near-real-time data fed off the internet.

*
The current iteration does not yet achieve the lofty goals that have been outlined above, but serve as a first step in going in that direction. 
It is hoped that with time and with a lot of testing that this tool has the potential to enable all architects to be lazy, playful, passionate procrastinators that we as creative types often wish to be.


- pre-requisites: Rhino and Grasshopper latest versions, Google Earth Pro(free), and a decent internet connection.


0. download entire .rar file onto your desktop
1. open grasshopper > file > special folders > components folder and paste contents of folder '2_plugins required' into the components folder
2. install ironpython from '3_ironpython required' and the associated site_packages (plugins). refer to instructions in the folder
3. restart Rhino and Grasshopper
4. load design_augmentation_tool_pre_alpha_v0.1.gh into grasshopper and wait for it to stop freezing.
5. copy the folder directory for the hong kong dataset with timelapse (in 4_example datasets). 
e.g:  I:\_FOR GITHUB_compilation 20170226\4_example datasets\hongkong dataset with timelapse
6. paste the address into the text panel in the blue group of the definition (leftmost)
7. tick all the relevant files that you want to use (do not tick temp_OCR, it is an automatically generated file for scaling)
8. press play
9. check out different sliders and stuff

9b. if you want to try looking at different areas of the world (read: anywhere in the world, but maybe not the north of south pole, sorry.), simple prepare datasets in a similar format to those found in the '4_example datasets' folder.
9.c often the minimum required dataset is one(1) osm file, one (1) jpeg file from google earth pro, and one(1) kml file. refer to 

10. think of what you would like to add to the design tool, and have a look at the file '5_roadmap'
11. send suggestions to tliqun@gmail.com

disclaimer: 
- openstreetmap doesn't always have all the building boundary info or building height info, so currently the script fills in the blanks with the equivalent of 3-5 storey heights
- there are currently no proper roads, only single polylines. i used to have a semi-working road generator for that, but due to it not beong robust enough, it was not included
 

known issues:
- home-brew python port of the coordinate conversion does not seem to match google earth imagery, and disparity increases as the scale of the model increases. actually gHowl might already be able to solve that but i haven't gone around to it yet.
- weimar example dataset has a super fancy tall structure sticking out of its city center according to osm, but i'm sure its a mismatch of info. will look into it in time.
