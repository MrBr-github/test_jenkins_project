def nodes = ['hpc-test-node', 'hpc-test-node2'] 
//git url: 'https://github.com/Mellanox/test_jenkins_projec'
//def projects = sh test_pipeline.sh get_job_list
def projects = ['a','b']

def builders = [:]

for ( x in projects ) {
  def proj = x
  builders[proj] = {
    node(hpc-test-node) {
       sh test_pipeline.sh do_job ${proj}
    }
  }
  
}