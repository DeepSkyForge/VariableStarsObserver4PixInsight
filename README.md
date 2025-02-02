# Variable Stars Observer for PixInsight 1.9.x

## Description
Variable Stars Observer is based on the well-known PixInsight Dynamic PSF process.
It provides PixInsight users with an easy way to estimate the magnitude of variable stars.

This is the first version.
I am seeking feedback from experienced astronomers in variable star analysis.

## Install
To install VariableStarsObserver in PixInsight 1.9.x, copy/past below URL
- `https://pixinsight.deepskyforge.com/update/variablestarsobserver/`

in PixInsight **RESOURCES > Updates > Manage Repositories**.
This will add new entry **VariableStarsObserver** in **PROCESS > ImageInspection**

DON'T FORGET THE TRAILING SLASH "/".
DO NOT TRY TO OPEN URL WITH A BROWSER (indeed, this will redirect you to the website).

VariableStarsObserver is __not__ compatible with PixInsight 1.8 and below versions.

## Usage

To use VariableStarsObserver, simply open an image in PixInsight and launch the VariableStarsObserver process from the menu **PROCESS > ImageInspection**.
In the process dialog box, click on the grey star button in the top right corner of the "Variable Stars Observer" section.}

The process will query the International Variable Stars Index to retrieve all variable stars available in the image's field of view.
It will then perform a second query to the AAVSO Plotter to retrieve all the constant stars and associated data.

Next, the process will perform a PSF (Point Spread Function) measurement on each constant and variable star.
The magnitude of the variable stars will be estimated based on the constant stars.
The stars will then be sorted by channel and magnitude (either reference magnitude or estimated magnitude).

The process will automatically select a variable star near the center of the image.
Constant stars with magnitudes close to the variable star will be automatically selected as comparison and check stars.
A new calculation of the variable star's magnitude will be performed based on selected compare star and displayed in the text box.

Text box provides following information based on stars selected in picklists:
- **Magnitude**: Estimation of the variable star magnitude based on the compare.
- **Mag. Cmp.**: Magnitude of compare star as reported by AAVSO.
- **Mag. Chk.**: Magnitude of check star as reported by AAVSO.
- **Chk. Mag.**: Estimation of the check star magnitude based on compare star.
- **Chk. Err.**: Difference between estimated and real check star magnitude (lower is better).

The user can click on the AAVSO Report button to generate a formal AAVSO report in Extended format.

# Documentation
You'll find full documentation [here](https://www.deepskyforge.com/vso/pixinsight/tools/VariableStarsObserver/VariableStarsObserver.html).

# Legal notice
Variable Stars Oberver process for PixInsight (c) Copyright 2024-2025 Joël Vallier\
This product is based on software from the PixInsight project, developed by Pleiades Astrophoto and its contributors [https://pixinsight.com/](https://pixinsight.com/).

THIS SOFTWARE IS PROVIDED BY PLEIADES ASTROPHOTO AND ITS CONTRIBUTORS
"AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED
TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR
PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL PLEIADES ASTROPHOTO OR ITS
CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL,
EXEMPLARY OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, BUSINESS
INTERRUPTION; PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; AND LOSS OF USE,
DATA OR PROFITS) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.
