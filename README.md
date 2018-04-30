# do-multi-upload-codeigntier

public function multiupload(){	
	$this->load->library('upload');
	 $path = './assets/images/';
	$this->upload->initialize(array(
			"upload_path"	=> $path,
			"allowed_types"=>"*"
		));
	
		//Perform upload.
		if($this->upload->do_multi_upload("files")) {
			//Code to run upon successful upload.
		print_r($this->upload->get_multi_upload_data());
		}
}
