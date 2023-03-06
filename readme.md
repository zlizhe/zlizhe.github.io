https://hexo.io/zh-cn/docs/one-command-deployment

New Post
hexo new ContentName

Deploy
hexo clean && hexo deploy

手动部署
hexo clean
hexo generate
cp -R public/.* github_page