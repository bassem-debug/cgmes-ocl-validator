# CGMES OCL rules V3 Validator Prototype

This project is a framework to automatize the validation of CGMES files using OCL rules. It uses the Eclipse EMF framework.

## Purpose

The goal of this tool is to provide some feedback to TSOs and RSCs about the quality
of data they generate or use.

## Installation

### Requirements

This tool requires Java >= 1.8.
It can be downloaded from https://www.java.com/fr/download/.

The tool has been tested under Windows and Linux.

### Package
Unzip the installation package wherever you want.
The installation package contains has the following structure:
----- config/
----- inputs/
----- ocl_validator/
----- validate.bat
----- validate.sh


## Configuration

- copy the input IGMS to be validated into the directory `inputs`. The format has to 
be the following: each xml profile instance file has to be in a separate zip file 
- *(optional)* copy in the directory `config` a CGMES boundary set (same format: each 
instance as a separate zip). This boundary set will be substituted to the one defined
in the IGM if this is not the same. This process is similar to what OPDE does.
- *(optional)* in case validation rules have been updated, a new version can be 
used to re-process data. It has to replace `config/cgmes61970oclModel.ecore`.

## Usage
###  Windows users
Run the following script
`validate.bat
`
### Linux users
Run the following script
`validate.sh
`

In both cases, during the execution, logs will be displayed on the screen.
The output of the CGMES file analysis is stored in an **Excel sheet** under the directory `inputs`. This xls file contains one sheet per IGM. 

For each IGM are reported: 
- the name of the violated rule, 
- the object class it applies to and 
- the rdf:id (and when possible the name) of the object instances it refers to.

## Disclaimer

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT OWNER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

## Copyright
&copy; ENTSO-E, RTE 2019
Authors: Lars-Ola Gottfried Österlund, Marco Chiaramello, Jérôme Picault

## License
to be defined

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
