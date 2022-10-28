Hi 👋

This terraform configuration file is for deploying the following resources in your AWS account.

1. Create vpc
2. Create Internet Gateway
3. Create Custom Route Table
4. Create a Subnet
5. Associate subnet with Route Table
6. Create Security Group to allow port 22,80,443
7. Create a network interface with an ip in the subnet that was created in step 4
8. Assign an elastic IP to the network interface created in step 7
9. Create Ubuntu server and install/enable apache2

          !! NOTE !!

          In 6, Instead of declaring two separate ingress blocks, we declared a single dynamic ingress block.
          We also specified the iterator argument as port If we had not done that, then we would have used ingress.
          value instead of port.value in the code since the default iterator is the label of the dynamic block.
          The repetition of dynamic blocks is generated from the for_each argument which say what variable to iterate over.
          The referenced variable should be a list or a map. 
          For lists, you can refer to the "value" of each member.
          For maps, you can refer to the "key" and "value" of each member. 
          The actual repeated block is generated from the nested content block



          For more details you always check-out my personal notion page on terraform
          https://www.notion.so/Terraform-01ed7b0002744dd1af6b36f368646ebc 
           
