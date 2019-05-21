# Ordo-ez-agenda
Agenda

string Nombre, Apellido, Direccion, Nacionalidad, Unidad_E;
        string cedula, telefono, correo, edad, ciclo, Estado_civ;
        int pos;
        int i = 1;
        //Guardamos los DATOS
        private void btnGuardar_Click(object sender, EventArgs e)
        {
            Nombre = txtNombre.Text;
            Apellido = txtApellido.Text;
            Direccion = txtDireccion.Text;
            Nacionalidad = txtNacionalidad.Text;
            cedula=txtCedula.Text;
            telefono = txttelefono.Text;
            correo = txtMail.Text;
            edad = txtEdad.Text;
            Unidad_E = txtUnidad_Edu.Text;
            ciclo = txtCiclo.Text;
            Estado_civ = cmbEstado_Civ.Text;
            if (cmbCarrera.SelectedIndex==0)
            {
                if (checkFeme.Checked==true)
                {
                    dataGridView1.Rows.Add(i,Nombre,Apellido, cedula, Nacionalidad,telefono,Unidad_E, correo, cmbCarrera.Text,txtCiclo.Text,checkFeme.Text, edad, cmbEstado_Civ.Text, Direccion,cmbTipo_sangre.Text);   
                }
                if (checkMascu.Checked==true)
                {
                    dataGridView1.Rows.Add(i, Nombre, Apellido, cedula, Nacionalidad, telefono, Unidad_E, correo, cmbCarrera.Text, txtCiclo.Text, checkMascu.Text, edad, cmbEstado_Civ.Text, Direccion,cmbTipo_sangre.Text);   
                }
                
            }
            if (cmbCarrera.SelectedIndex==1)
            {
                if (checkFeme.Checked == true)
                {
                    dataGridView1.Rows.Add(i, Nombre, Apellido, cedula, Nacionalidad, telefono, Unidad_E, correo, cmbCarrera.Text, txtCiclo.Text, checkFeme.Text, edad, cmbEstado_Civ.Text, Direccion, cmbTipo_sangre.Text);
                }
                if (checkMascu.Checked == true)
                {
                    dataGridView1.Rows.Add(i, Nombre, Apellido, cedula, Nacionalidad, telefono, Unidad_E, correo, cmbCarrera.Text, txtCiclo.Text,checkMascu.Text, edad,cmbEstado_Civ.Text, Direccion,cmbTipo_sangre.Text);
                }
                
            }
            if (cmbCarrera.SelectedIndex==2)
            {
                if (checkFeme.Checked == true)
                {
                    dataGridView1.Rows.Add(i, Nombre, Apellido, cedula, Nacionalidad, telefono, Unidad_E, correo, cmbCarrera.Text, txtCiclo.Text,checkFeme.Text, edad, cmbEstado_Civ.Text, Direccion,cmbTipo_sangre.Text);
                }
                if (checkMascu.Checked == true)
                {
                    dataGridView1.Rows.Add(i, Nombre, Apellido, cedula, Nacionalidad, telefono, Unidad_E, correo, cmbCarrera.Text, txtCiclo.Text, checkMascu.Text, edad, cmbEstado_Civ.Text, Direccion,cmbTipo_sangre.Text);
                }
                
            }
            i++;
           
        }
        //
        private void dataGridView1_CellContentClick(object sender, DataGridViewCellEventArgs e)
        {
            pos = dataGridView1.CurrentRow.Index;
             if (cmbCarrera.SelectedIndex==0)
            {
                 cmbCarrera.Text = dataGridView1[1, pos].Value.ToString();
            }
             if (cmbCarrera.SelectedIndex==1)
             {
                 cmbCarrera.Text = dataGridView1[1, pos].Value.ToString();
             }
             if (cmbCarrera.SelectedIndex==2)
             {
                 cmbCarrera.Text = dataGridView1[1, pos].Value.ToString();
             }
             if (cmbCarrera.SelectedIndex==3)
             {
                 cmbCarrera.Text = dataGridView1[1, pos].Value.ToString();
             }
                txtNombre.Text=dataGridView1[1,pos].Value.ToString();
                txtApellido.Text=dataGridView1[2,pos].Value.ToString();
                txtCedula.Text = dataGridView1[3, pos].Value.ToString();
                txtNacionalidad.Text = dataGridView1[4, pos].Value.ToString();
                txttelefono.Text = dataGridView1[5, pos].Value.ToString();
                txtUnidad_Edu.Text = dataGridView1[6, pos].Value.ToString();
                txtMail.Text = dataGridView1[7, pos].Value.ToString();
                txtCiclo.Text = dataGridView1[9, pos].Value.ToString();
                if (checkFeme.Checked==true)
                {
                    checkFeme.Text = dataGridView1[10, pos].Value.ToString();
                }
                if (checkMascu.Checked==true)
                {
                    checkMascu.Text = dataGridView1[10, pos].Value.ToString();
                }
                txtEdad.Text = dataGridView1[11, pos].Value.ToString();
                cmbEstado_Civ.Text = dataGridView1[12, pos].Value.ToString();
                txtDireccion.Text = dataGridView1[13, pos].Value.ToString();
                cmbTipo_sangre.Text = dataGridView1[14, pos].Value.ToString();

        }

        private void btnEditar_Click(object sender, EventArgs e)
        {
            if (cmbCarrera.SelectedIndex==0)
            {
                dataGridView1[1, pos].Value = cmbCarrera.Text;
            }

            if (cmbCarrera.SelectedIndex == 1)
            {
                dataGridView1[1, pos].Value = cmbCarrera.Text;
            }

            if (cmbCarrera.SelectedIndex == 2)
            {
                dataGridView1[1, pos].Value = cmbCarrera.Text;
            }
            dataGridView1[1, pos].Value = txtNombre.Text;
            dataGridView1[2, pos].Value = txtApellido.Text;
            dataGridView1[3, pos].Value = txtCedula.Text;
            dataGridView1[4, pos].Value = txtNacionalidad.Text;
            dataGridView1[5, pos].Value = txttelefono.Text;
            dataGridView1[6, pos].Value = txtUnidad_Edu.Text;
            dataGridView1[7, pos].Value = txtMail.Text;
            dataGridView1[9, pos].Value = txtCiclo.Text;
            if (checkFeme.Checked==true)
            {
                dataGridView1[10, pos].Value = checkFeme.Text;
            }
            if (checkMascu.Checked==true)
            {
                dataGridView1[10, pos].Value = checkMascu.Text;
            }
            dataGridView1[11, pos].Value = txtEdad.Text;
            dataGridView1[12, pos].Value = cmbEstado_Civ.Text;
            dataGridView1[13, pos].Value = txtDireccion.Text;
            dataGridView1[14, pos].Value = cmbTipo_sangre.Text;
        }

        private void btnEliminar_Click(object sender, EventArgs e)
        {
            dataGridView1.Rows.RemoveAt(pos);
        }

        private void button1_Click(object sender, EventArgs e)
        {
            limpiar();
            cmbCarrera.Text = "";
            cmbEstado_Civ.Text = "";
            txtCiclo.Text = "";
        }
        private void limpiar()
        {
            txtNombre.Text = "";
            txtApellido.Text = "";
            txtCedula.Text = "";
            txtDireccion.Text = "";
            txtEdad.Text = "";
            txtNacionalidad.Text = "";
            txttelefono.Text = "";
            txtUnidad_Edu.Text = "";
            txtMail.Text = "";
        }

        private void txtNombre_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (!char.IsLetter(letra)&& letra!=13 && letra!=8 && letra !=32)
            {
                e.Handled = true;
            }
        }

        private void txtApellido_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (!char.IsLetter(letra) && letra != 13 && letra != 8 && letra != 32)
            {
                e.Handled = true;
            }
        }

        private void txtDireccion_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (!char.IsLetter(letra) && letra != 13 && letra != 8 && letra != 32)
            {
                e.Handled = true;
            }
        }

        private void txtCedula_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (char.IsLetter(letra) && letra != 13 && letra != 8 && letra != 32)
            {
                e.Handled = true;
            }
        }

        private void txtNacionalidad_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (!char.IsLetter(letra) && letra != 13 && letra != 8 && letra != 32)
            {
                e.Handled = true;
            }
        }

        private void txttelefono_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (char.IsLetter(letra) && letra != 13 && letra != 8 && letra != 32)
            {
                e.Handled = true;
            }
        }

        private void txtUnidad_Edu_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (!char.IsLetter(letra) && letra != 13 && letra != 8 && letra != 32)
            {
                e.Handled = true;
            }
        }

        private void txtMail_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (!char.IsLetter(letra) && letra != 13 && letra != 8 && letra != 32)
            {
                e.Handled = true;
            }
        }

        private void txtEdad_KeyPress(object sender, KeyPressEventArgs e)
        {
            char letra = e.KeyChar;
            if (char.IsLetter(letra) && letra != 13 && letra != 8 && letra != 32)
            {
                e.Handled = true;
            }
        }

        private void grp2_Enter(object sender, EventArgs e)
        {
            if (checkFeme.Checked==true)
            {
                checkMascu.Enabled = false;
            }
        }

        private void checkMascu_MouseClick(object sender, MouseEventArgs e)
        {
            if (checkMascu.Checked == true)
            {
                checkFeme.Enabled = false;
            }
        }

        private void checkFeme_MouseClick(object sender, MouseEventArgs e)
        {
            if (checkFeme.Checked == true)
            {
                checkMascu.Enabled = false;
            }
        }
