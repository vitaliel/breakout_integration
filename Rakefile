# Re ticket1
#
task :default => :commit

def commit_one
  File.open("ftest.txt", "a") do |f|
    f.write "hello\n"
  end

  `git add . && git-commit -a -m "message-#{Time.now.to_i}, re #1" --author "Username <username@host.com>"`
end

task :commit do
  commit_one
  sleep 2
  commit_one
end

# Trosk
