from flask import Flask, request
from flask import render_template

app = Flask(__name__)
users = [{'username': 'admin1', 'password':'123456'}, {'username': 'guest', 'password':'123456'}]

@app.route('/')
def main():
    return render_template('index.html')

@app.route('/login', methods=['GET', 'POST'])
def login():
	username= request.form['username']
	password= request.form['password']
	for user in users:
		if user['username'].lower() == username.lower() and user['password'] == password:
			return render_template('success.html', username=username)
		else :
			return render_template('failure.html')


if __name__ == '__main__':
	app.run()
