Bug link: https://issuetracker.unity3d.com/issues/android-build-fails-when-there-are-680-or-more-files-in-the-streaming-assets-folder  
Issue ID: 1272592

I tested on several versions of unity to find the one that is causing the problem and it's the version 2020.1.0f1  
-2020.1.17f1: Build failed  
-2020.1.0f1: Build failed  
-2019.4.16f1: Build succeeded  
-2019.4.10f1: Build succeeded  
-2019.2.17f1: Build succeeded

Here the changelog: https://unity3d.com/fr/unity/whats-new/2020.1.0

It may be a regression from this patch https://issuetracker.unity3d.com/issues/android-loading-assets-from-assetbundles-takes-significantly-more-time-when-the-project-is-built-as-an-aab

To reproduce the bug, start a build.  
If the folder sudoku3x2(in streaming assets folder) is removed, the build succeeded
