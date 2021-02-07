# 3DPO Dataset

Qualitative dataset focused on textureless, 3D printed objects. Intended to be used to evaluate monocular 6DoF tracking techniques in very difficult scenarios.

Originally published in VISAPP 2021 as part of the full paper entitled *Real-time Monocular 6DoF Tracking of Textureless Objects Using Photometrically-enhanced Edges*. **BibTeX for citation:**

> @inproceedings{valenca2021real,
  title={Real-time Monocular 6DoF Tracking of Textureless Objects Using Photometrically-enhanced Edges},
  author={Valenca, Lucas and Silva, Luca and Chaves, Thiago and Gomes, Arlindo and Figueiredo, Lucas and Cossio, Lucio and Tandel, Sebastien and Lima, Joao Paulo and Simoes, Francisco and Teichrieb, Veronica},
  booktitle={16th International Conference on Computer Vision Theory and Applications (VISAPP)},
  year={2021}
}

To see the spotlight video showcasing real-time trackers working on the 3DPO dataset, please see the video below:
https://www.youtube.com/watch?v=PGJkgiA23Z0

For licensing and credits, please see the `LICENSE.txt` file.

**Contact Person:** Lucas Valença (*lucas@valenca.io* or *lvrma@cin.ufpe.br*)

## Objects
All objects used were 3D printed after the CAD models (with the exception of the Glass Bottle). Material colors were determined after the 3D printing filaments.

The rendered objects, their names, and the amount of vertices can be seen in the figure `assets/objects.png`. All OBJ and MTL files can be found in  the `assets` folder.

## Sequences
Sequences were recorded with one or more objects on both clear and cluttered backgrounds with challenges such as: *fast motion, motion blur, clipping, occlusion, handling, refraction, multiple viewpoint changes,* and *independent object-camera motion.*

Detailed descriptions and snapshots of each sequence can be seen in the figure `sequences/cheat_sheet.png`.

All sequences can be found in VGA resolution, PNG frame-by-frame format under the following naming scheme: `sequences/sequence_name/sequence_name_%04d.png`.

## Poses and Camera
The camera calibration can be found in `assets/calibration.yml`.

Initial 6DoF poses for every main object in every sequence (and frame-by-frame ground truth for **Slow**) can be found in the `poses` folder.

Because of the complexity of the scenes, there is no ground truth beyond the first frame. The idea is to see which techniques are able to make it through which sequences until the end. The exception is the sequence **Slow**, in which there's ground truth for every frame thanks to unoccluded binary markers and sufficiently slow, non-blurry camera motion.