[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=15&duration=666&pause=500&color=2AF7A6CC&multiline=true&random=false&width=500&height=500&lines=%5Bx%5D+Initializing+HackTool+v3.1.5...;%5Bx%5D+Target%3A+pentagon.gov;%5Bx%5D+Scanning+for+vulnerabilities...;%5Bx%5D+Open+port+found%3A+443+%28HTTPS%29;%5Bx%5D+Deploying+payload+via+SSL%2FTLS+exploitation...;%5Bx%5D+Payload+delivered+successfully.;%5Bx%5D+Establishing+secure+connection...;%5Bx%5D+Connection+established.;%5Bx%5D+Bypassing+firewall...;%5Bx%5D+Firewall+bypassed.+Accessing+internal+network...;%5Bx%5D+Searching+for+sensitive+data...;%5Bx%5D+Classified+documents+found.;%5Bx%5D+Downloading+files...;%5Bx%5D+Download+complete.+Files+saved+to+%2Fmnt%2Fsecure_vault;%5Bx%5D+Covering+tracks...;%5Bx%5D+Tracks+erased.+Disconnecting...;%5Bx%5D+Operation+completed+successfully.+System+integrity+100%25+intact.;)](https://git.io/typing-svg)

`python3 script.py target.txt`
```python
import sys
import urllib.parse

def transform_text(input_text):
    # Replace spaces with '+' and separate lines with ';'
    transformed = input_text.replace(" ", "+").replace("\n", ";")

    # Encode special characters
    transformed = urllib.parse.quote(transformed, safe='+;')

    # Embed in the URL format used in the example
    url_format = '[![Typing SVG](https://readme-typing-svg.demolab.com?font=Fira+Code&size=15&pause=1000&color=2AF7A6CC&multiline=true&random=false&width=500&height=500&lines={})](https://git.io/typing-svg)\n'
    transformed = url_format.format(transformed)

    return transformed

def transform_file(input_file_path, output_file_path='OUTPUT.md'):
    try:
        with open(input_file_path, 'r') as file:
            input_text = file.read()
    except IOError as e:
        return f"Error reading file {input_file_path}: {e}"

    transformed_text = transform_text(input_text)

    try:
        with open(output_file_path, 'w') as file:
            file.write(transformed_text)
    except IOError as e:
        return f"Error writing to file {output_file_path}: {e}"

    return f"Transformation complete. Output saved to {output_file_path}"

if __name__ == "__main__":
    if len(sys.argv) != 2:
        print("Usage: python transform_text_to_md.py <input_file_path>")
        sys.exit(1)

    input_file_path = sys.argv[1]
    result = transform_file(input_file_path)
    print(result)
```
