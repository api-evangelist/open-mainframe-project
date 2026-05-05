---
title: "Welcome to the Mainframe Software Hub for Linux"
url: "https://openmainframeproject.org/blog/welcome-to-the-mainframe-software-hub-for-linux/"
date: "Thu, 05 Mar 2026 16:00:00 +0000"
author: "Open Mainframe Project"
feed_url: "https://openmainframeproject.org/feed/"
---
<div class="wpb_row vc_row-fluid vc_row" id="fws_69eb93ed3515c" style="padding-top: 0px; padding-bottom: 0px;"><div class="row-bg-wrap"><div class="inner-wrap row-bg-layer"><div class="row-bg viewport-desktop"></div></div></div><div class="row_col_wrap_12 col span_12 dark left">
	<div class="vc_col-sm-12 wpb_column column_container vc_column_container col no-extra-padding inherit_tablet inherit_phone flex_gap_desktop_10px ">
		<div class="vc_column-inner">
			<div class="wpb_wrapper">
				
<div class="wpb_text_column wpb_content_element ">
	<p><span style="font-weight: 400;">Ever try to find a binary, container, or package for a piece of open source software for Linux on the mainframe, but find that none exist?</span></p>
<p><span style="font-weight: 400;">The new Open Mainframe Project Mainframe Software Hub for Linux is here to address this!</span></p>
<p><span style="font-weight: 400;">Across the open source ecosystem there are people contributing to the technical enablement of open source software packages for IBM Linux on the mainframe architecture (s390x). Through this work over the decades that Linux has been supported on the platform, we’ve seen thousands of projects enabled, many of which are either included in Linux distributions today, or release binaries, containers, and packages through their own project channels. Unfortunately, that leaves thousands of projects which either don’t fit neatly into the vision of the Linux distributions, or that of the project maintainers who have limited resources for supporting hardware architectures.</span></p>
<p><span style="font-weight: 400;">This has led to organizations across the mainframe ecosystem maintaining and sharing build scripts and patches, and ultimately building packages themselves for use by themselves or their clients. The Mainframe Software Hub for Linux is a centralized project that allows organizations to have a vendor-neutral home for these build scripts and patches, and a release mechanism so that binaries, containers, and other packages can be found in one location.</span></p>
<p><span style="font-weight: 400;">A new project and GitHub organization has been created at</span><a href="https://github.com/linuxonzapps"> <span style="font-weight: 400;">https://github.com/linuxonzapps</span></a><span style="font-weight: 400;"> to host this work and currently hosts a small collection of binaries for download.</span></p>
<p><span style="font-weight: 400;">To kick things off, Rishi Misra has begun with a handful of select projects that have build scripts and patches long been maintained by IBM, and residing on the</span><a href="https://github.com/linux-on-ibm-z/docs/wiki"> <span style="font-weight: 400;">linux-on-ibm-z GitHub wiki</span></a><span style="font-weight: 400;">.</span></p>
<h2><b>How to Download the Software</b></h2>
<p><span style="font-weight: 400;">At the current phase of this project, we don’t have a unified interface for downloading the packages that are made available. Instead, we’re using GitHub’s releases mechanism to manage these downloads.</span></p>
<p><span style="font-weight: 400;">To see if the software you’re seeking is available, follow these steps:</span></p>
<ol>
<li style="font-weight: 400;"><span style="font-weight: 400;">Go to </span><a href="https://github.com/linuxonzapps"><span style="font-weight: 400;">https://github.com/linuxonzapps</span></a></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Search the project names to see if one matches the project you want.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Click on the project name and go to the Releases page in the right-hand side of the screen.</span></li>
<li style="font-weight: 400;"><span style="font-weight: 400;">Download the version that’s been made available.</span></li>
</ol>
<p><span style="font-weight: 400;">As a reminder, all the work is completed and released under the Apache 2.0 license and while we welcome bug reports if you discover an issue, this software is provided under those conditions, including: “on an ‘AS IS’ BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND”. As with all software you integrate into your environment, we strongly recommend you run your own functionality and security evaluation.</span></p>
<h2><b>How to Develop with Us</b></h2>
<p><span style="font-weight: 400;">As mentioned above, build scripts and patches for each project are referenced in their own project repository inside the linuxonzapps repository. The</span><a href="https://github.com/linuxonzapps/zlinux-artifacts-builder"> <span style="font-weight: 400;">zlinux-artifacts-builder</span></a><span style="font-weight: 400;"> that has been developed takes these scripts and patches and creates releases that can be downloaded by members of the community who wish to use the software.</span></p>
<p><span style="font-weight: 400;">Let’s open up the</span><a href="https://github.com/linuxonzapps/bazel"> <span style="font-weight: 400;">linuxonzapps Bazel</span></a><span style="font-weight: 400;"> repository to see how it works from the developer side.</span></p>
<p><span style="font-weight: 400;">Within this repository, we have the </span><span style="font-weight: 400;">src/</span><span style="font-weight: 400;"> directory that includes a </span><span style="font-weight: 400;">build.sh</span><span style="font-weight: 400;"> file with the s390x-specific build instructions. In this initial launch, it’s pulling in a </span><span style="font-weight: 400;">build_bazel.sh</span><span style="font-weight: 400;"> script that still resides on the linux-on-ibm-z/scripts repository.</span></p>
<p><span style="font-weight: 400;">From there, take a look at the </span><span style="font-weight: 400;">.build-template.yaml</span><span style="font-weight: 400;"> file which defines which version to build, and the container image to use for the build.</span></p>
<p><span style="font-weight: 400;">By running this YAML file through the zlinux-artifacts-builder, a binary released through the releases mechanism provided by GitHub and is immediately made available for download.</span></p>
<p><span style="font-weight: 400;">The zlinux-artifacts-builder can do much more than that though. It can be extended to support building custom binaries, DEB packages, RPM packages, and container images, the tool gives developers the flexibility to cater their releases specifically to their target audience for consuming the packages. Check out the</span><a href="https://github.com/linuxonzapps/zlinux-artifacts-builder/blob/main/README.md"> <span style="font-weight: 400;">zlinux-artifacts-builder README</span></a><span style="font-weight: 400;"> for more about usage, and trying it out yourself.</span></p>
<h2><b>Learn More</b></h2>
<p><span style="font-weight: 400;">We’re in the very early stages of this project, so now is a great time to make an impact.</span></p>
<p><span style="font-weight: 400;">You can get started today by joining our mailing list at</span><a href="https://lists.openmainframeproject.org/g/mainframe-software-hub-discussion"> <span style="font-weight: 400;">https://lists.openmainframeproject.org/g/mainframe-software-hub-discussion</span></a><span style="font-weight: 400;"> where we share meeting announcements, updates to the builder, and other ideas.</span></p>
<p><span style="font-weight: 400;">Then dig deeper by looking at general documentation for the project at</span><a href="https://github.com/linuxonzapps/docs"> <span style="font-weight: 400;">https://github.com/linuxonzapps/docs</span></a></p>
<p><span style="font-weight: 400;">And find further details about our Technical Steering Committee, along with information about our monthly meetings can be found at</span><a href="https://github.com/linuxonzapps/tsc"> <span style="font-weight: 400;">https://github.com/linuxonzapps/tsc</span></a></p>
<p><span style="font-weight: 400;">We can’t wait to share and build some s390x binaries with you!</span></p>
</div>




			</div> 
		</div>
	</div> 
</div></div>
<p>The post <a href="https://openmainframeproject.org/blog/welcome-to-the-mainframe-software-hub-for-linux/">Welcome to the Mainframe Software Hub for Linux</a> appeared first on <a href="https://openmainframeproject.org">Open Mainframe Project</a>.</p>
