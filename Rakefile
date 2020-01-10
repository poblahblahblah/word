deploy_default = "s3"
s3_bucket       = "words.tetrisblocks.net"
aws_cli_path    = "/usr/local/bin/aws"
aws_region      = "us-west-1"

desc "Deploy website via aws s3 sync"
task :s3 do
  puts "## Deploying website via aws s3 sync"
  system("#{aws_cli_path} s3 sync src/ s3://#{s3_bucket}/ --region #{aws_region} --profile madelinefox")
end

desc "Deploy files to S3"
task :deploy => [:s3]
task :default => :deploy
