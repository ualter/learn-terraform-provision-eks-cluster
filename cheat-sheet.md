# Configure kubectl
aws eks --region $(terraform output region | sed -e 's/^"//' -e 's/"$//') update-kubeconfig --name $(terraform output cluster_name | sed -e 's/^"//' -e 's/"$//')