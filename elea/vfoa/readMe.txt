Raw data per group can be extracted from the zip file (rawData/vfoa_aftersync.zip) and the computed features are stored in Matlab structures.


rawData/
	vfoa_aftersync.zip Contains the visual attention raw data per frame, each txt file corresponds to each group.
	vfoa_aftersyncNotation.txt Contains the notation used in the raw data.

features/
*Visual Features
	vfoaGiven_Rec.mat	Contains the amount of attention received and given per participant
	vfoaGiven_Rec_smooth.mat	Contains the amount of attention received and given per participant (using smooth parameters)
	vfoa40_entireMeeting.mat	Contains the computed visual attention features per participant

	Gaze features notation (referred as Visual Attention features).
	ATR or attentionReceived: Received Attention is the number of frames in which the participant i is looked by the other participants.
	ATG or attentionGive: Given Attention (ATG) is the number of frames in which a participant i looks at other participants.
	ATQ Attention Quotient or Attention ratio: is the ratio between the amount of attention that participant i received from the other participants (ATR) and the amount of attention that participant i gives to the other participants in the group (ATG).
	ATC Center of Attention (ATC) is the total number of frames in which participant i received attention from all the participants in the group at the same time.


*Multimodal Features, i.e. Visual Attention and Speaking Cues
	lws_lwl40.mat Contains the synchronized audio and visual attention features per group.

	Multimodal features notation.
	looking while speaking (lws): Amount of attention (in frames) that participant i gives to the participants in the group while i is speaking.
	looking while not speaking (lwl): Amount of attention (in frames) that participant i gives to the participants in the group while i is not speaking. Note that we cannot infer that a person is listening, so we simply approximate this by non-speaking.
being looked at while speaking (blws): Amount of attention that participant i receives from the other participants while i is speaking.
	center of attention while speaking (caws): Number of frames that participant i is the center of attention (i.e. all the participants are looking at her/him at the same time) while i is speaking.
	visual dominance ratio (vdr): Ratio of Looking while Speaking and Looking while Listening (lws/lwl).


--------------------------------------------------
For details on extraction and performance see:

-Jayagopi, D., Sanchez-Cortes, D., Otsuka, K., Yamato, J., & Gatica-Perez, D. (2012, October). Linking speaking and looking behavior patterns with group composition, perception, and performance. In Proceedings of the 14th ACM international conference on Multimodal interaction (pp. 433-440). ACM

-Sanchez-Cortes, D., Aran, O., Jayagopi, D. B., Mast, M. S., & Gatica-Perez, D. (2013). Emergent leaders through looking and speaking: from audio-visual data to multimodal recognition. Journal on Multimodal User Interfaces, 7(1-2), 39-53.
