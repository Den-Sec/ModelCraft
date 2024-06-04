# ModelCraft - Ai 3D Model Maker

ModelCraft is an innovative tool designed to simplify the creation of 3D models using OpenSCAD. By utilizing advanced language models, ModelCraft transforms natural language prompts into precise OpenSCAD scripts. This automation enables users, from beginners to professionals, to quickly generate complex 3D models without deep knowledge of coding. The tool also integrates seamlessly with Cura, allowing users to preview and fine-tune their models before printing.

---

### Features

- **Natural Language to 3D Model**: Generate OpenSCAD scripts from user prompts.
- **Script Cleaning**: Ensures the generated OpenSCAD script is valid and free of unnecessary formatting.
- **Automated Model Generation**: Converts OpenSCAD scripts into 3D model files (STL).
- **Integration with Cura**: Opens generated STL files in Cura for preview and further adjustments.

---

### Prerequisites

Before using ModelCraft, ensure you have the following installed:

- **Python 3.x**
- **OpenSCAD**: A script-only 3D CAD modeler.
- **Cura**: A slicing application for 3D printers.
- **Dotenv**: To manage environment variables.

You can install the required Python packages using:

`pip install python-dotenv requests`

---

### Setup

1. **Clone the Repository**:
    
    `git clone https://github.com/yourusername/modelcraft.git cd modelcraft`
    
2. **Environment Variables**:
    
    Create a `.env` file in the root directory and configure the following variables:
    
```
    OLLAMA_URL=<your_ollama_api_url> 
    MODEL_NAME=<your_model_name> 
    OPENSCAD_PATH=<path_to_openscad_executable> 
    CURA_PATH=<path_to_cura_executable>
```
    
3. **Run the Tool**:
    
    `python modelcraft.py`
    

---

### Usage

1. **Run the Script**:
    
    Execute the script using Python:
    
    `python modelcraft.py`
    
2. **Enter a Prompt**:
    
    When prompted, enter a description of the 3D model you want to create. For example:
    
    `Enter your prompt for the 3D model: A simple cube with a side length of 20mm.`
    
3. **Generated OpenSCAD Script**:
    
    The tool will output the generated OpenSCAD script:
    
    `OpenSCAD script generated: cube([20, 20, 20]);`
    
4. **Model Generation**:
    
    The OpenSCAD script is cleaned and used to generate an STL file. The tool will confirm once   the model is generated:
    
    `3D model generated and saved as output.stl`
    
5. **Preview in Cura**:
    
    The generated STL file is automatically opened in Cura for preview and further adjustments:
    
    `Opening output.stl in Cura...`
    

---

### Error Handling

- **API Errors**: If the API request to Ollama fails, ensure your environment variables are correctly configured and that the API endpoint is accessible.
- **OpenSCAD Execution Errors**: If OpenSCAD fails to generate the model, ensure the OpenSCAD executable path is correct and that the script is valid.
- **Cura Execution Errors**: If Cura fails to open the STL file, ensure the Cura executable path is correct and that Cura is installed.

---

### Contributing

We welcome contributions to enhance ModelCraft. Feel free to fork the repository, create feature branches, and submit pull requests.

---

### License

This project is licensed under the MIT License. See the LICENSE file for details.

---

### Contact

For questions or support, please open an issue on the GitHub repository or contact the maintainer at dennis.sepede@outlook.com.

---

Happy Modeling with ModelCraft!
