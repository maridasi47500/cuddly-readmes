🧠 Project Overview: *C’est moi*

A personal setup guide combining Bash, Python, Ruby, and Markdown tools for
development and logging.
⚙️ Setup Instructions🖋️ Markdown to HTML
bash

sudo apt install markdown discount
vi README.md  # Write your content
mkd2html "README.md" "readme"

🐍 Python Environment & Flask Server
bash

python3 -m venv tutorial-env
source tutorial-env/bin/activate
flask run --host=0.0.0.0

💎 Ruby IRB History Logging
ruby

Kernel.at_exit {
  File.open("irb.log", "w") do |f|
    f << Readline::HISTORY.to_a.join("\n")
  end
}


   -

   This saves your IRB input history to irb.log upon exit.
   -

   For persistent history, add to ~/.irbrc:

ruby

IRB.conf[:SAVE_HISTORY] = 1000

🐍 Python History Logging
python

import readline
readline.write_history_file('python_history.txt')

🧩 Notes & Tips

   -

   When writing content: → Start your keywords in the *title*, end them in
   the *body*. → Replace shapes (square, circle, triangle) with emojis of
   your choice.
   -

   For data logging: → Fill your table once per GPS position, datetime, and
   full dataset.

🧭 README Focus

Start by choosing your direction:  *Frontend (HTML)* or *Backend
(Python/Ruby)*.
