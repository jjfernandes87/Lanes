## O que voce pode fazer com essas lanes?

#### Alterar o numero da versão

- `change_version_number`: Change version number with prompt
- `patch`: Increment by one the project version number (ex: 2.0.1 => 2.0.2)
- `minor`: Increment by one the project version number (ex: 2.0.1 => 2.1.0)
- `major`: Increment by one the project version number (ex: 2.0.1 => 3.0.0)
- `bump`: Increment build number

#### Gerenciar seu repositorio cocoapods

- `install_private_repo`: Install you private pods repository on your mac or on the CI
- `publish_pod`: Publish a new version of you pod automatically
- `tag_and_pod`: Publish a new version of you pod automatically after creating a new tag based on the project version number
- `lint_pod`: Lint the .podspec

## Como usar
### Configuração do projeto

Para usar nossas lanes, adicione a linha no topo do seu fastfile:

	import_from_git(url: 'git@github.com:YOUR_USERNAME/lanes.git', path: 'fastlane/Fastfile') 

	def cocoapods 
	{
		private_repo: "my_private_repo",
    	private_repo_name: "my_private_repo",
		private_repo_git_url: "git@github.com:MyTeam/my_private_repo.git",
		podspec: "./MyPod.podspec",
		pod_name: "MyPod"
	}

### Para usar a lane

	fastlane THE_NAME_OF_THE_LANE