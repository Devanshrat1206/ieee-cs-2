from flask import Flask, render_template, request, jsonify

app = Flask(__name__)

@app.route('/')
def home():
    return render_template('amazon.html')

@app.route('/toggle_dark_mode', methods=['POST'])
def toggle_dark_mode():
    dark_mode = request.json.get('dark_mode')
    return jsonify({'message': 'Dark mode toggled successfully'})

if __name__ == '__main__':
    app.run(debug=True)
