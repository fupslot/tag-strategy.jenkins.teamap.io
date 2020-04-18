### Github Tag Strategy


### Commands
  `**/tags/*`

- `COMMIT_ID=$(git rev-list --tags --date-order | head -1)`
- `TAG=$(git show-ref --tags | grep $COMMIT_ID | awk -F / '{print $NF}')`

- `docker build -t teamapio/tag-strategy:$TAG .`
- `docker push teamapio/tag-strategy:$TAG`