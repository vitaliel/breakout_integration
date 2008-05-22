task :default => :commit

task :commit_one do
  File.open("ftest.txt", "a") do |f|
    f.write "hello"
  end
  `git add . && git-commit -a -m "message-#{Time.now.to_i}"`
end

task :commit do
  Rake::Task['commit_one'].invoke
  sleep 2
  Rake::Task['commit_one'].invoke
end
